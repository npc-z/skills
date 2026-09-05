---
name: scoped-commit
description: >
  Write a scoped commit message — scope first, terse, no type prefix.
  Use for "write a commit", "commit message", /commit or /scoped-commit.
---

Write commit messages terse and exact. Lead with the **scope** — the project area the change touches — not a type. Scope is the subject; type is redundant. Why over what.

## Steps

1. **Read the diff.** Pull the full diff, the changed files, and `git status`. Completion: every changed file and the whole diff is in view.
2. **Name the scope.** The one project-relevant area the diff touches: subsystem, package path, microservice, or component. It should be self-evident from the changed files. Completion: a single noun phrase you can verify against the diff.
3. **Write the subject.** `<scope>: <imperative summary>`. Completion: ≤50 chars (hard 72), imperative mood, no trailing period, no type prefix, and a scope that names what changed.
4. **Decide the body.** Skip when the subject is self-explanatory. Add only for non-obvious *why*, breaking changes, migrations, or a link to issues. Completion: either the subject explains the change alone, or the body carries the why.
5. **Output as a code block.** Ready to paste, not committed. Completion: the message is rendered.

## Rules

**Subject:**
- `<scope>: <imperative summary>` — scope is mandatory; it is the subject
- No type prefix (`feat:`, `fix:`, `refactor:`). The description already carries the type, and a single change is often more than one type
- Imperative: "add", "fix", "remove" — not "added", "adds", "adding"
- ≤50 chars, hard cap 72
- No trailing period
- Match project convention for capitalization after the colon

**Scope:**
- Use project shorthand: Go → package path, Linux → subsystem, microservices → service name
- One scope, the narrowest that covers the diff; if the change spans areas, use the area the change is about
- Drop the file name when the scope already says it

**Body — only if needed:**
- Non-obvious *why*, breaking changes, data migrations, reverts
- Wrap at 72 chars
- Bullets `-`, not `*`
- Link issues at the end: `Closes #42`, `Refs #17`

**Auto-clarity:**
- Always include a body for breaking changes, security fixes, data migrations, and anything reverting a prior commit. Never compress these into subject-only — future debuggers need the context.

## Examples

Diff: new endpoint for the user profile
- ❌ `feat(api): add a new endpoint to get user profile information from the database`
- ✅
  ```
  api: add GET /users/:id/profile

  Mobile client needs profile data without the full user payload to
  cut LTE bandwidth on cold-launch screens.

  Closes #128
  ```

Diff: breaking route rename
- ✅
  ```
  api: rename /v1/orders to /v1/checkout

  BREAKING CHANGE: clients on /v1/orders must migrate to /v1/checkout
  before 2026-06-01. Old route returns 410 after that date.
  ```

## Guardrails

Never include:
- "This commit does X", "I", "we", "now", "currently" — the diff says what changed; state what it does, never narrate it
- "As requested by..." — use a `Co-authored-by` trailer instead
- AI attribution ("Generated with Claude Code") unless the user's own rule requires it
- Emoji, unless project convention requires
- A type prefix — scope is the subject; the type never leads

## Boundaries

Only generates the commit message. Does not run `git commit`, does not stage files, does not amend. Output the message as a code block ready to paste. "stop scoped-commit" or "normal mode": revert to the project's verbose commit style.
