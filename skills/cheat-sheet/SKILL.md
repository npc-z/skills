---
name: cheat-sheet
description: "Compress any topic into a one-page cheat sheet: definitions, rules, examples, common mistakes, and quick-test questions. Use when the user needs a scannable reference for fast review."
disable-model-invocation: true
argument-hint: "What topic should the cheat sheet cover?"
---

# One-Page Cheat Sheet

This skill compresses any topic into a single scannable page — perfect before an exam, meeting, interview, or real-world task.

## Workflow

1. Ask what topic to compress (if not provided)
2. Ask if there's a specific context (exam, interview, project)
3. Generate the cheat sheet in the format below
4. Verify it's under 500 words
5. Offer to print or save as a reference file

**Completion**: A cheat sheet under 500 words, scannable (headers + bullets + short phrases), with a 5-question quick test at the end.

## Output Format

```markdown
# [TOPIC] Cheat Sheet

## Definitions
- **Term**: concise definition (one line each)

## Rules
- The non-obvious rules you must remember
- If-then statements for quick reference

## Examples
- One concrete example per key concept
- Show, don't explain

## Common Mistakes
- What most people get wrong
- The exception to the rule

## Quick Test
1. [question]
2. [question]
3. [question]
4. [question]
5. [question]
```
