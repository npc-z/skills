---
name: 20-hour-plan
description: "Find the core 20% of any topic that unlocks 80% of results, structured into 10 study sessions of 2 hours each. Use when the user wants a focused study plan."
disable-model-invocation: true
argument-hint: "What topic should be planned into 20 hours?"
---

# Learn Anything in 20 Hours

Most subjects have a small set of ideas that unlock everything else.

This skill finds that core 20% first, then turns it into a 10-session, 2-hour-per-session learning plan.

## Principles

- **Core 20% first** — find what unlocks the rest
- **10 sessions, 2 hours each** — structured and actionable
- **Each session has**: objective, concepts, exercises, resources, review questions
- **Sequential build** — each session depends on the previous

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

## Workflow

1. Ask what topic to plan (if not provided)
2. Ask about the user's available time and goals
3. Identify the core 20% of the topic
4. Structure it into 10 sequential sessions
5. For each session, write the objective, concepts, exercises, resources, and review questions
