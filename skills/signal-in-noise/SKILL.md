---
name: signal-in-noise
description: "Find the 5 highest-leverage resources for any topic — books, videos, courses, communities. Stop collecting, start using. Use when the user needs to pick the right learning resources before starting."
disable-model-invocation: true
argument-hint: "What topic do you need resources for?"
---

# Find the Signal in the Noise

There are thousands of resources for every topic. Most people waste time collecting instead of learning.

This skill finds the 5 that matter and builds a path using only those 5.

## Principles

- **Quality over quantity** — 5 resources, not 50
- **Ranked by leverage** — highest impact first
- **Actionable** — each resource tied to a specific learning goal
- **No filler** — if it doesn't move the needle, it's noise

## Output Format

```markdown
# Resources for [TOPIC]

## The 5

1. **[Title]** (type: book/video/course/community)
   - Why: [one sentence on why this is the best use of time]
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

## Workflow

1. Ask what topic the user wants to learn
2. Ask about their current level and goals
3. Find and rank 5 resources
4. Build a 7-day path using only those 5
5. Tell them: "Use these 5. Ignore everything else until you're done."
