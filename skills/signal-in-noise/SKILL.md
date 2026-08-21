---
name: signal-in-noise
description: "Find the 5 highest-leverage resources for any topic. Stop collecting, start using. Use when the user needs to pick learning resources before starting."
disable-model-invocation: true
argument-hint: "What topic do you need resources for?"
---

# Find the Signal in the Noise

Separate signal from noise: find the 5 resources that matter and build a path using only those 5.

## Workflow

1. Ask what topic the user wants to learn
2. Ask about their current level and goals
3. Find and rank 5 resources — each tied to a specific learning goal
4. Build a 7-day path using only those 5
5. State clearly: "Use these 5. Ignore everything else until you're done."

**Completion**: The user has 5 ranked resources with links and a 7-day path. Each resource has a stated learning goal.

## Output Format

```markdown
# Resources for [TOPIC]

## The 5

1. **[Title]** (type: book/video/course/community)
   - Signal: [one sentence on why this is the highest-leverage pick]
   - What you'll learn: [specific outcome]
   - Link: [URL or access method]

2. ...

## 7-Day Path

| Day | Resource | Focus |
|-----|----------|-------|
| 1 | #1 | [specific topic] |
| 2 | #1 | [specific topic] |
| ... | ... | ... |
```
