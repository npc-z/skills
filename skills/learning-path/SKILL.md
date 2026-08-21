---
name: learning-path
description: Create structured learning paths with skill ladders and 20-hour plans. Use when user wants to learn a new topic, needs a learning roadmap, or wants to break down a complex subject into manageable stages.
---

# Learning Path Generator

Create structured learning paths that prevent common learning failures: skipping fundamentals, lacking direction, or burning out on advanced topics before mastering basics.

## When to Use

- User says "I want to learn [topic]"
- User asks "How should I approach learning X?"
- User needs a roadmap for a new skill
- User feels overwhelmed by a complex subject

## Two-Phase Approach

### Phase 1: Skill Ladder (5 Levels)

Break the topic into 5 clear difficulty levels. For each level, provide:

1. **Level name** (Beginner → Confident Practitioner)
2. **What you should understand** at this stage
3. **What mastery looks like** — concrete evidence of competence
4. **Key concepts/skills** to focus on
5. **Milestone project** proving readiness to advance
6. **Practice exercise** for hands-on learning
7. **Common mistakes** learners make at this level
8. **Self-check question** before moving to next level

**Level Structure:**
- Level 1: Complete Beginner
- Level 2: Basic Understanding
- Level 3: Practical User
- Level 4: Problem Solver
- Level 5: Confident Practitioner

### Phase 2: 20-Hour Intensive Plan (80/20法则)

After the skill ladder, create a focused 20-hour plan:

1. **Identify the 20%** that yields 80% of practical results
2. **Create 10 learning stages**, each 2 hours
3. For each stage include:
   - Main learning objective
   - Key concepts to master
   - Practice exercise or mini-project
   - Recommended resource (free/beginner-friendly)
   - Expected outcome after completion
4. **5 review questions** at the end of each stage
5. **Final capstone project** demonstrating real-world competence

## Output Format

Save the learning path to `LEARNING-PATH.md` in the current directory with:

```markdown
# Learning Path: [Topic]

## Skill Ladder

### Level 1: [Name]
**What to understand:** ...
**Mastery looks like:** ...
**Key concepts:** ...
**Milestone:** ...
**Practice:** ...
**Common mistakes:** ...
**Self-check:** ...

[repeat for all 5 levels]

## 20-Hour Intensive Plan

### Core 20% (The Vital Few)
- [concept 1]
- [concept 2]
...

### Stage 1 (Hours 1-2): [Title]
**Objective:** ...
**Key concepts:** ...
**Practice:** ...
**Resource:** ...
**Expected outcome:** ...
**Review questions:**
1. ...
2. ...
3. ...
4. ...
5. ...

[repeat for all 10 stages]

## Capstone Project
[description of final project]
```

## Principles

- **Practical over theoretical** — every concept ties to real application
- **Beginner-friendly language** — avoid unnecessary jargon
- **Progressive difficulty** — each level builds on the previous
- **Concrete evidence** — milestones are measurable, not abstract
- **Fast feedback** — exercises provide immediate sense of progress
