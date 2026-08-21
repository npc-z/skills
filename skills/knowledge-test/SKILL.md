---
name: knowledge-test
description: Test understanding through active recall and Feynman technique. Use when user wants to verify knowledge, find knowledge gaps, or deeply understand a topic through explanation.
---

# Knowledge Testing & Deep Understanding

Test what you actually know vs what you think you know. Two complementary methods: progressive questioning and Feynman explanation loop.

## When to Use

- User says "Test my understanding of [topic]"
- User wants to find knowledge gaps before an exam/interview
- User says "Explain like I'm 5" or wants Feynman method
- User feels they understand something but can't explain it simply

## Method 1: Progressive Questioning

Act as a strict but supportive examiner. One question at a time, increasing difficulty.

### Question Progression

| Difficulty | Questions | Purpose |
|------------|-----------|---------|
| Beginner | 1-3 | Foundation check |
| Intermediate | 4-6 | Core understanding |
| Advanced | 7-8 | Depth & nuance |
| Expert | 9-10 | Edge cases & synthesis |

### For Each Answer

1. **Score** (1-10)
2. **What was correct** — reinforce strengths
3. **Identify gaps** — pinpoint exact knowledge holes
4. **Re-explain** — teach the missed part in simple language
5. **Follow-up** — if weak, ask a probing question before moving on

### Final Report

After all questions, provide:
- Final score
- Strongest areas
- Weakest areas
- Brief review plan
- 5 challenge questions for mastery

## Method 2: Feynman Learning Loop

If you can't explain it simply, you don't understand it well enough.

### The Loop

1. **Explain** — User explains the topic in their own words, as if to a 12-year-old
2. **Review** — Agent checks for:
   - Correct parts (reinforce)
   - Knowledge gaps (identify)
   - Confusions or errors (correct)
   - Missing concepts (note)
3. **Teach back** — Agent re-teaches only the missed parts using simple language
4. **Repeat** — User explains again, clearer this time
5. **Continue** until explanation is simple, accurate, and complete

### Rules

- Don't advance until explanation is clear
- Don't overwhelm with extra theory
- Correct gently but clearly
- Use examples when confusion arises
- End with a clean, saved explanation

## Output Format

Save test results to `KNOWLEDGE-TEST.md`:

```markdown
# Knowledge Test: [Topic]

## Progressive Questions

### Q1 (Beginner)
**Question:** ...
**Your answer:** ...
**Score:** X/10
**What was correct:** ...
**Knowledge gap:** ...
**Re-explanation:** ...

[repeat for all questions]

### Final Summary
- **Total score:** X/100
- **Strongest:** ...
- **Weakest:** ...
- **Review plan:** ...

## Feynman Explanation

### Attempt 1
[User's explanation]

### Gaps Identified
- ...

### Corrected Understanding
[Agent's re-teaching]

### Attempt 2 (Final)
[User's improved explanation]

### Final Explanation
[Clean version saved for reference]
```

## Principles

- **Active recall over passive review** — testing builds stronger memory
- **One question at a time** — prevents cognitive overload
- **Immediate feedback** — close the loop tight
- **Simple language** — if it needs jargon, you don't understand it yet
- **No shame in gaps** — they're opportunities, not failures
