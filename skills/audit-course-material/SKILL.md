---
name: audit-course-material
description: Fact-check, error-check and correct education material. Use whenever a user asks to review, audit, fact-check, proofread, find errors in, verify the math of, or improve a course, lesson, textbook, chapter, handout, test, quiz, workbook, answer key, study guide or exam-prep material, at any level or field. Produces a double-checked correction report and a corrected version.
---

# Audit course material

Follow `rules/source-integrity.mdc` at every step. It is required, not optional.

## Inputs
- The material (required), supplied by the user. Record title, edition, date, level, field and location markers (page, line, section, question number).
- Optional: jurisdiction, exam or standard version (for example "Series 7 outline, current edition", "NEC 2023"), sources the user trusts.

## Workflow
1. **Gate (laws and platform rules).** Confirm the user supplied the material. If it looks like confidential exam content or proprietary prep material the user may not share, stop and say so. Quote only short excerpts in the report.
2. **Identify field and level.** Open `references/field-guide.md`, pick the row(s) that apply, and note the authoritative sources and the current version and date to check against.
3. **Extract.** List every checkable item with its location: facts, names, dates, figures, money amounts, rule and statute numbers, formulas, calculations, cross-references, numbering, commands and UI steps, answer-key answers.
4. **Check facts.** Use the highest source tier available. Record source title, issuing body, version or date, and where in it the answer is. Reject unreliable sources.
5. **Recompute the math.** Redo each calculation from its inputs. Show the steps. Separate rounding from real errors.
6. **Check internal consistency.** Cross-references, numbering, settings changed in one step and assumed later, answer keys vs the text.
7. **Flag outdated material.** Any rule, limit, rate, code edition, guideline or software version that changed since publication. Give the current value and its effective date.
8. **Double-check.** For each finding, do a second independent check: a second independent source, or a recomputation by a different method, or a recheck of the original text. Status:
   - `CONFIRMED`: two independent checks agree.
   - `SINGLE-CHECK`: only one check possible.
   - `UNVERIFIED`: no legitimate source reachable. Never guess.
   - `WITHDRAWN`: the second check showed the material was right. Keep it in the report so the reasoning is visible.
9. **Classify.** Type (`fact`, `math`, `outdated`, `unclear`, `typo`, `structure`), severity (`high` teaches a wrong answer or fails a student, `medium` misleading, `low` cosmetic) and confidence (`high`, `medium`, `low`).
10. **High-stakes label.** For medical, legal and financial findings add "Review aid, not professional advice. Needs expert confirmation."
11. **Write the correction report** with `references/report-template.md`: original (exact quote), correction, check 1, check 2, status, type, severity, confidence.
12. **Write the improved version.** Apply only CONFIRMED corrections, tagged `[corrected: #N]`. Mark SINGLE-CHECK and UNVERIFIED items `[check: #N]` and leave the text unchanged.
13. **Summarize.** Counts by status, type and severity; unverified list; what was not checked; versions and dates of the sources used.

## Edge cases
- Huge documents: audit in chunks by chapter or section; keep one running issue list with global numbering; state which parts were covered.
- Scanned PDFs: extract text with `pdftotext` (poppler); if there is no text layer, OCR with free tesseract if available, otherwise ask for a text copy. Mark OCR-dependent quotes SINGLE-CHECK.
- Non-English material: check against sources in the same language and jurisdiction; do not translate before quoting the original.
- Conflicting sources: prefer the higher tier and the newer effective date; report the conflict and both sources; status SINGLE-CHECK if unresolved.
- Paywalled sources: never bypass a paywall. Use a free authoritative alternative, or mark UNVERIFIED and name the source that would settle it.

## Severity scoring
Score = impact (3 teaches a wrong answer or fails a student, 2 misleading, 1 cosmetic) x reach (3 core concept or tested item, 2 example, 1 aside). 6-9 high, 3-4 medium, 1-2 low.

## Export
On request, also output the issue table as JSON (array of objects with fields: id, location, type, severity, score, original, correction, check1, check2, status, confidence) or CSV with the same columns.

## Guardrails
- Never invent sources, quotes, rule numbers or page numbers.
- Never reproduce copyrighted or confidential exam questions or proprietary prep material.
- Style preferences are `unclear` at low severity, not errors.
- Free tools only. No paid APIs. No Google or Facebook account is required.

## Worked examples
`examples/echo-findings.md` (re-verified findings, including one withdrawn) and `examples/sample-report.md` (a full run).

## Language
Answer in the user's language; keep commands, file names, header and format names, and status labels unchanged. See the Language section of the rule file. For material in another language, quote and correct it in its own language and explain in the user's language.
