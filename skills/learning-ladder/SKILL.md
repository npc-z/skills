---
name: learning-ladder
description: "Break any topic into 5 difficulty levels with milestones and self-checks. Use when the user wants to know where they are and what's next in a learning journey."
disable-model-invocation: true
argument-hint: "What topic should be mapped into levels?"
---

# Learning Ladder

Most people fail at learning because they jump into advanced material before the basics are solid.

This skill maps any topic into 5 clear levels so you always know exactly where you stand.

## The 5 Levels

| Level | Name | What it covers |
|-------|------|----------------|
| 1 | Complete Beginner | The absolute first thing you need to know |
| 2 | Basic Understanding | Core concepts that unlock the rest |
| 3 | Practical Application | How to actually use this |
| 4 | Advanced Concepts | What separates beginners from practitioners |
| 5 | Confident Practitioner | What mastery looks like |

## Output Format

```markdown
# Learning Ladder: [TOPIC]

## Level 1: Complete Beginner
- **What you'll learn**: [one sentence]
- **Milestone**: [how you know you've reached it]
- **Self-check**: [a quick test to verify readiness]

## Level 2: Basic Understanding
...

## Level 3: Practical Application
...

## Level 4: Advanced Concepts
...

## Level 5: Confident Practitioner
...
```

## Workflow

1. Ask what topic to map (if not provided)
2. Ask about the user's current experience level
3. Generate the 5 levels with milestones and self-checks
4. Help the user identify their current level
5. Point them to what's next
