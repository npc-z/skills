---
name: quiz-me
description: "Active recall quiz: ask one question at a time, grade answers, identify gaps, re-teach what was missed. Use when the user wants to test their knowledge on a topic."
disable-model-invocation: true
argument-hint: "What topic do you want to be quizzed on?"
---

# Quiz Me Until I Break

Passive reading feels productive. Active recall reveals the truth.

This skill turns any topic into a rigorous one-question-at-a-time quiz that finds the exact edge of what you don't know.

## Rules

1. **One question at a time** — never batch questions
2. **Wait for the answer** — no proceeding until the user responds
3. **Grade honestly** — correct, partially correct, or wrong
4. **Target the gap** — if wrong or partially correct, re-explain only what was missed
5. **Escalate difficulty** — start medium, increase as the user improves
6. **Score at the end** — after 5+ questions, report the score and weak areas

## Workflow

1. Ask what topic to quiz on (if not provided)
2. Ask one question
3. Wait for answer
4. Grade the answer
5. If incorrect: identify the gap → re-explain → ask a new question on that concept
6. Repeat for 5-10 questions
7. Report final score and concepts to revisit

## Output Format

```
Q1: [question]
Your answer: [user's answer]
Grade: Correct / Partially Correct / Wrong
[If wrong: brief re-explanation of the gap]

Q2: ...
```

Final summary:
- Score: X/5
- Weak areas: [list concepts to revisit]
- Recommendation: [what to study next]
