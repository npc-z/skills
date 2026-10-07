---
name: implement-and-review-loop
description: "Implement the work in a spec or tickets, run the two-axis code review, then loop caveman-review until a round comes back clean."
disable-model-invocation: true
argument-hint: "What should I implement?"
---

Implement the work described by the user in the spec or tickets, then converge it through a **caveman-review loop**. The main agent implements and fixes; one dedicated reviewer only reviews. Nothing is committed unless the user explicitly asks.

## Steps

1. **Read the ticket.** If the user passed a ticket reference, fetch it from the issue tracker and state its title before starting. If the reference is ambiguous, ask. Completion: the ticket's title is stated, or there is no ticket reference to resolve.
2. **Implement.** Call the Skill tool with `tdd` where possible, at pre-agreed seams. Run typechecking regularly, single test files regularly, and the full test suite once at the end. Completion: the full suite passes and every item in the spec or tickets is implemented.
3. **Pin the fixed point.** Capture the one command that shows the reviewer the whole change — `git diff HEAD` while the work is uncommitted, or `git diff <base>...HEAD` if it was committed — plus the commit list. Make new files visible (`git add -N .`, or hand the reviewer `git status`). Completion: an exact diff command, confirmed non-empty and covering every changed and new file.
4. **Run the two-axis review.** Call the Skill tool with `code-review` against that fixed point. Fix every finding. Completion: each Standards and Spec finding is fixed, or declined with a one-line reason.
5. **Dispatch the reviewer.** Start one **review-only subagent** and keep it for the whole loop. Its prompt carries the working directory, the pinned diff command, and its mandate: call the Skill tool with `caveman-review` on the current diff and return the findings, nothing else. Completion: the first round's findings are in hand.
6. **Drive the loop.**
   - Fix every finding the reviewer returns. Answer a `❓ q:`, or decline a `🔵 nit:` with a one-line reason.
   - `send_message` the same subagent: the round's resolutions, then a fresh `caveman-review` pass over the current diff, reporting only **new** findings.
   - Repeat until a round returns nothing — a **clean round**. That round ends the loop.

   Completion: one clean round reported and quoted in the final write-up.
7. **Report.** State the implemented items, the two-axis outcome, each loop round (findings and resolution), the clean round, the test/typecheck result, and that nothing was committed.

## Loop rules

**The reviewer only reviews.** It never edits code, runs linters, approves, or commits. A fix worth debating comes back as `❓ q:`.

**One reviewer for the loop.** Dispatch it once and reach it with `send_message`; its memory of earlier rounds is what tells a *new* finding apart from one already resolved.

**Fresh eyes each round.** Every round re-reviews the whole current diff, not just the last fix — a fix can surface a finding elsewhere.

**Feed resolutions back.** Name each fix and each decline, so resolved findings are not re-raised.

**A clean round ends it.** The loop stops on the first round with no findings; skip further polish passes. If a round repeats a finding already reported fixed, the loop has stalled — stop and report the impasse instead of re-fixing blind.

**Never commit.** Leave the work in the working tree. Commit only when the user explicitly asks for it.
