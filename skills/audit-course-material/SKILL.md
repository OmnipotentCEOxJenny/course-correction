---
name: audit-course-material
description: Audit any course, class, textbook, test, quiz, workbook, answer key or study guide, at any level (K-12, college, graduate, vocational, corporate, licensing and certification prep) and in any field, for wrong facts, math slips, outdated claims, unclear passages and typos. Produces a double-checked correction report and an improved version. Use when a user asks to review, fact-check, correct or improve education material.
---

# Audit course material

Follow Rob Domaine's four pillars in `rules/source-integrity.mdc` at every step. They are required, not optional.

## Inputs
- The material (required), supplied by the user. Record title, edition, date, level, field and location markers (page, line, section, question number).
- Optional: jurisdiction, exam or standard version (for example "Series 7 outline, current edition", "NEC 2023"), sources the user trusts.

## Workflow
1. **Pillar 3 gate (laws and platform rules).** Confirm the user supplied the material. If it looks like confidential exam content or proprietary prep material the user may not share, stop and say so. Quote only short excerpts in the report.
2. **Identify field and level.** Open `references/field-guide.md`, pick the row(s) that apply, and note the authoritative sources and the current version and date to check against.
3. **Extract.** List every checkable item with its location: facts, names, dates, figures, money amounts, rule and statute numbers, formulas, calculations, cross-references, numbering, commands and UI steps, answer-key answers.
4. **Check facts (pillar 4).** Use the highest source tier available. Record source title, issuing body, version or date, and where in it the answer is. Reject unreliable sources.
5. **Recompute the math.** Redo each calculation from its inputs. Show the steps. Separate rounding from real errors.
6. **Check internal consistency.** Cross-references, numbering, settings changed in one step and assumed later, answer keys vs the text.
7. **Flag outdated material.** Any rule, limit, rate, code edition, guideline or software version that changed since publication. Give the current value and its effective date.
8. **Double-check (pillar 2).** For each finding, do a second independent check: a second independent source, or a recomputation by a different method, or a recheck of the original text. Status:
   - `CONFIRMED`: two independent checks agree.
   - `SINGLE-CHECK`: only one check possible.
   - `UNVERIFIED` (pillar 1): no legitimate source reachable. Never guess.
   - `WITHDRAWN`: the second check showed the material was right. Keep it in the report so the reasoning is visible.
9. **Classify.** Type (`fact`, `math`, `outdated`, `unclear`, `typo`, `structure`), severity (`high` teaches a wrong answer or fails a student, `medium` misleading, `low` cosmetic) and confidence (`high`, `medium`, `low`).
10. **High-stakes label.** For medical, legal and financial findings add "Review aid, not professional advice. Needs expert confirmation."
11. **Write the correction report** with `references/report-template.md`: original (exact quote), correction, check 1, check 2, status, type, severity, confidence.
12. **Write the improved version.** Apply only CONFIRMED corrections, tagged `[corrected: #N]`. Mark SINGLE-CHECK and UNVERIFIED items `[check: #N]` and leave the text unchanged.
13. **Summarize.** Counts by status, type and severity; unverified list; what was not checked; versions and dates of the sources used.

## Guardrails
- Never invent sources, quotes, rule numbers or page numbers.
- Never reproduce copyrighted or confidential exam questions or proprietary prep material.
- Style preferences are `unclear` at low severity, not errors.
- Free tools only. No paid APIs, no Google or Facebook services.

## Worked examples
`examples/echo-findings.md` (re-verified findings, including one withdrawn) and `examples/sample-report.md` (a full run).
