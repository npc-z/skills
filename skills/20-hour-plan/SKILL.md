---
name: 20-hour-plan
description: "Find the core 20% of any topic that unlocks 80% of results, structured into 10 sessions of 2 hours each. Use when the user wants a focused study plan."
disable-model-invocation: true
argument-hint: "What topic should be planned into 20 hours?"
---

# Learn Anything in 20 Hours

This skill finds the core 20% of a topic, then structures it into 10 sessions of 2 hours each.

## Workflow

1. Ask what topic to plan (if not provided)
2. Ask about the user's available time and goals
3. Identify the core 20% — the concepts that unlock the rest
4. Structure it into 10 sequential sessions, each building on the previous
5. For each session, write: objective, key concepts (3-5), exercises, resources, review questions

**Completion**: 10 sessions are written, each with a clear objective, 3-5 key concepts, at least one exercise, and 3 review questions. Every session depends on the previous one.

## Output Format

```markdown
# 20-Hour Plan: [TOPIC]

## Core 20%
[What are the key concepts that unlock 80% of this topic?]

## Session Plan

### Session 1: [Title]
- **Objective**: [one sentence]
- **Key concepts**: [3-5 bullet points]
- **Exercises**: [what to do, not just read]
- **Resources**: [which resource to use]
- **Review questions**: [3 questions to answer from memory]

### Session 2: [Title]
...
```
