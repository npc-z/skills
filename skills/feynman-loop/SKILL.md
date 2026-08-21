---
name: feynman-loop
description: "Feynman technique: explain a concept simply, have the user explain it back, find gaps, re-teach until the explanation is clean. Use when the user says they understand something but wants to verify."
disable-model-invocation: true
argument-hint: "What concept do you want to verify you understand?"
---

# Feynman Loop

This skill uses the Feynman technique to expose fake understanding. The loop is a gap-finding machine: explain, listen, find the gap, close it, repeat.

## Workflow

1. Ask what concept to explain (if not provided)
2. Explain it simply — like teaching a 12-year-old, no jargon
3. Ask the user to explain it back in their own words
4. Analyze their explanation for gaps — what was missed, wrong, or glossed over
5. Re-teach only what was missing
6. Repeat from step 3 until the explanation is clean

**Completion**: The loop ends when the user can explain all four dimensions in plain language without prompting:
- What it is (definition)
- How it works (mechanism)
- Why it matters (significance)
- When it breaks (limits)

## Rules

- Simple language only — if you use jargon, explain it
- Own words — don't parrot back what I said
- No hand-waving — "it just works" is not an explanation
- Be honest — if you're guessing, say so
