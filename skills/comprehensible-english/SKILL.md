---
name: comprehensible-english
description: "Explain hard English with plain-English scaffolding, then give the translation at the end."
disable-model-invocation: true
argument-hint: "Which English word, phrase, or passage should I explain?"
---

# Comprehensible English

Help the learner read hard English. The explanation stays in English — a paraphrase, then plain-English glosses — because that is where the reading happens; the translation at the end confirms the meaning.

**The ladder** (English side): original → paraphrase → gloss → grammar detail. Climb only as high as comprehension requires.

## Steps

1. **Find the blockers.** Take the learner's word, phrase, or passage — ask for one if it is missing — and name what blocks comprehension: an unusual meaning, a phrasal verb, an idiom, a meaning-bearing collocation or grammatical structure, or any word the learner asks about. Completion: a list of blockers, each with the reason it blocks this learner.
2. **Paraphrase the meaning.** Restate it in more frequent, familiar English — a formal noun phrase becomes a plain verb phrase — keeping the original's meaning, tense and aspect, modality, negation, and logical links. Completion: nothing added, nothing dropped, every difficult word replaced by an easier one, and the result reads as natural adult English.
3. **Gloss the blockers.** One plain-English line each for the words, phrases, idioms, and collocations; a blocker that is the shape of the sentence goes to `### Grammar`. Completion: every blocker accounted for — glossed here or explained in `### Grammar` — and no gloss harder than the expression it explains.
4. **Translate.** Into the learner's native language, inferred from the conversation — default Chinese when it cannot be told. Completion: a translation is present, in that language, carrying the natural meaning rather than a word-for-word mapping.

## Output

```markdown
### Original
[the learner's text, verbatim]

### Comprehensible English
[the paraphrase]

### Key Help
- `expression` → plain-English gloss

### Translation
[natural translation]
```

Place `### Grammar` above `### Translation`, so the translation stays last.

## Example

The common case — the glosses leave the original readable:

```markdown
### Original
The committee conducted a thorough investigation into the matter, but the manager had already gone to ground.

### Comprehensible English
The committee tried hard to find out what had happened, but the manager had already gone into hiding.

### Key Help
- `conduct an investigation` → try to find out what happened
- `the matter` → the situation being discussed
- `go to ground` → hide so that nobody can find you

### Translation
委员会对此事进行了彻底调查，但那位经理已经躲了起来。
```

The structural case — the obstacle is the shape of the sentence:

```markdown
### Original
Not until the auditors had gone did the manager admit that the figures had been doctored.

### Comprehensible English
The manager admitted that the figures had been changed dishonestly — but only after the auditors had gone.

### Key Help
- `doctored` → changed dishonestly
- `auditors` → people who check a company's accounts

### Grammar
`Not until … did the manager admit …` — starting a sentence with `Not until` moves the auxiliary in front of the subject (`did the manager admit`), the same word order as a question. The meaning is that the admission came only after the auditors had gone.

### Translation
直到审计人员离开，经理才承认账目被人做了手脚。
```

## Rules

**The original is authoritative.** Quote it verbatim, oddities included — literary, colloquial, archaic, domain-specific. Corrections and simplifications live in the paraphrase.

**Gloss chunks.** `run out of` is one unit; `kick the bucket` → "to die". Explain only the blockers — annotating every token raises the load the scaffold exists to lower.

**Preserve useful difficulty.** Keep subordinate and relative clauses, conditionals, passive voice, and discourse links: `He did not want to accept the offer` beats `He said no`. Simplify vocabulary first; reach for syntax only when vocabulary alone leaves the meaning out of reach.

**Grammar carries the structural blockers.** When the obstacle is the shape of the sentence rather than a word in it — inversion, a clause whose attachment is unclear, a construction whose shape is the whole difficulty — it shows how the sentence is built, with register, nuance, or etymology where they bear on it. When the paraphrase and glosses leave the original readable, the reply ends at the translation.

**Match the learner's level.** A known level sets the vocabulary and how simply the English side is pitched:

| Level | Explanation |
| --- | --- |
| A1–A2 | very common words, short sentences, concrete |
| B1 | simple but natural; gloss uncommon words; keep useful grammar |
| B2 | English-first; nuance and collocations |
| C1+ | keep most of the original structure; subtle meaning, register, idiom, style |

Unknown level: B1-style, and ask only when the level materially changes the answer.
