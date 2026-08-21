---
name: learn-10x
description: "Router for the accelerated learning system. Dispatches to signal-in-noise, learning-ladder, 20-hour-plan, quiz-me, cheat-sheet, or feynman-loop. Use when the user wants to learn a new skill or topic."
disable-model-invocation: true
argument-hint: "What would you like to learn?"
---

# Learn Anything 10x Faster

A structured learning system. Random Q&A produces random learning — real learning needs a path, tests, compression, and feedback loops.

This is a router. It has no workflow of its own. It dispatches to other skills.

## Phase 1: Plan

| Step | Skill | What it does |
|------|-------|--------------|
| 1 | `signal-in-noise` | Pick 5 resources, ignore the rest |
| 2 | `learning-ladder` | Map 5 difficulty levels with milestones |
| 3 | `20-hour-plan` | Core 20% in 10 sessions × 2 hours |

## Phase 2: Practice

| Need | Skill | When to use |
|------|-------|-------------|
| Test what I learned | `quiz-me` | After each study session |
| Compress for review | `cheat-sheet` | Before exam, meeting, or interview |
| Verify I truly understand | `feynman-loop` | When something feels shaky |

## How to Use

1. Ask: "Where do you want to start?"
2. Suggest the appropriate skill based on their answer:
   - "I'm just starting" → `signal-in-noise` → `learning-ladder` → `20-hour-plan`
   - "I've been studying, test me" → `quiz-me`
   - "Summarize this for me" → `cheat-sheet`
   - "I think I get it, but not sure" → `feynman-loop`
3. Let the user pick, or recommend the next logical step

**Completion**: The user has selected a skill and the router has dispatched.

## Recommended Flow

signal-in-noise → learning-ladder → 20-hour-plan → study session → quiz-me / cheat-sheet / feynman-loop → next session → repeat
