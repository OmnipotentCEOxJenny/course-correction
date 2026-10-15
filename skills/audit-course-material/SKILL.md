---
name: audit-course-material
description: Audit a course document, class handout, textbook chapter or section for wrong facts, math slips, outdated claims, unclear passages and typos. Produces a sourced correction report and an improved corrected version. Use when a user asks to review, fact-check, correct or improve course material.
---

# Audit course material

## Trigger
The user supplies a course, class, textbook chapter or section (file, pasted text or path) and wants it checked and corrected.

## Inputs
- The material (required). Record its title, edition and location markers (page, line, section).
- Optional: subject level, publication date, sources the user trusts.

## Workflow
1. **Extract.** List every checkable item with its location: factual claims, named people and organizations, dates, figures, money amounts, formulas, worked calculations, cross-references (for example "see Table 13.1"), section numbering, and commands or UI steps.
2. **Check facts.** For each claim, look for a legitimate primary source (see `rules/source-integrity.mdc`). Record the source title and where in it the answer is. If no source can be reached, mark the item UNVERIFIED. Never make one up.
3. **Recompute the math.** Redo every calculation from its stated inputs. Show inputs, steps and result. Note rounding effects separately from real errors.
4. **Check internal consistency.** Do cross-references point to the right table or figure? Is section numbering continuous? Do later steps contradict earlier setup (for example a setting turned off and never turned back on)?
5. **Flag outdated material.** Note claims tied to a date, version, price, law or software release that may have changed. Give the date of the source used for the update.
6. **Classify each issue.**
   - Type: `fact`, `math`, `outdated`, `unclear`, `typo` (use `structure` for numbering or cross-reference gaps).
   - Severity: `high` (teaches a wrong answer or would fail a student), `medium` (misleading or confusing), `low` (cosmetic).
   - Confidence: `high` (primary source or exact recomputation), `medium` (strong secondary or internal evidence), `low` (judgment call), `unverified`.
7. **Write the correction report** using `references/report-template.md`: one row per issue with location, original, correction, source or method, type, severity, confidence.
8. **Write the improved version** of the material: apply only corrections at medium or high confidence, mark each change inline as `[corrected: issue #N]`, and leave UNVERIFIED items unchanged with a `[check: issue #N]` note.
9. **Summarize**: counts by type and severity, a list of unverified items, and what was not checked.

## Guardrails
- Never invent sources, quotes or page numbers. "Unverifiable with available sources" is a valid result.
- Do not mark the original author wrong on style alone; style goes under `unclear` at low severity.
- Keep the original text intact in the report so every change can be reviewed.
- Free tools only. No paid APIs, no Google or Facebook services.

## Worked examples
See `examples/echo-findings.md` for real findings (DaVinci Resolve training book, project management textbook, technical writing textbook) and `examples/sample-report.md` for a full run.
