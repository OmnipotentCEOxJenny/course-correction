---
name: check-quiz-and-test
description: Check a quiz, test or answer key that goes with course material. Finds wrong or incomplete key answers, ambiguous questions, and questions built on a known book error. Use after an audit or when a user asks to verify a test or answer key.
---

# Check quiz and test

## Workflow
1. Pair each question with the passage it tests (section, page or line).
2. Answer each question independently from the source before reading the key.
3. Compare with the key. Flag: `key-wrong`, `key-incomplete`, `key-too-narrow`, `ambiguous-question`, `depends-on-book-error`.
4. For math questions, recompute and show the work.
5. Cross-check against any correction report: a question that relies on a corrected passage needs a rewrite.
6. Output a table: question number, issue, evidence (location), suggested fix, confidence.

## Guardrails
- A key can be wrong. Do not assume the key or the book is right; cite the passage.
- Never invent sources. Mark unresolvable questions UNVERIFIED.

## Example
A DaVinci Resolve test key was checked against the book: the Q13 key said fade handles "appear on every video clip", but audio clips have them too (book L5244), so that answer was too narrow. The Q12 key left out the Create Transition Preset step (L3895). Both are `key-incomplete` or `key-too-narrow`, high confidence.
