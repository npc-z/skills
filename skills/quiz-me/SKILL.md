---
name: quiz-me
description: "Active recall quiz: ask one question at a time, grade answers, identify gaps, re-teach what was missed. Use when the user wants to test their knowledge on a topic."
disable-model-invocation: true
argument-hint: "What topic do you want to be quizzed on?"
---

# Quiz Me Until I Break

This skill turns any topic into a rigorous one-question-at-a-time quiz. Every question targets the gap — the exact edge of what you don't know.

## Workflow

1. Ask what topic to quiz on (if not provided)
2. Ask one question
3. Wait for answer — never proceed until the user responds
4. Grade the answer: correct, partially correct, or wrong
5. If incorrect: identify the gap → re-explain only what was missed → ask a new question on that concept
6. Repeat for 5-10 questions, escalating difficulty as the user improves
7. Report final score, weak areas, and what to study next

**Completion**: After 5+ questions, produce a final summary with score (X/5), weak areas, and recommendation.

## Rules

- One question at a time — never batch
- Grade honestly — partially correct is not correct
- Close the gap — re-explain only what was missed, not the whole topic
- Escalate difficulty — start medium, increase as the user improves
