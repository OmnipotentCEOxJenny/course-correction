# Changelog

## 1.1.14 (2026-10-23)
- README: new "Testing status" section. Local automated tests pass; in-app testing is not yet completed. Records that the marketplace submit form's "tested locally and in-app" confirmation (2026-10-14) was checked in error before any in-app test; in-app testing is pending.
- Docs only; no behavior changes. Local tests re-run and passed. Not tested in-app. Not resubmitted.

## 1.1.13 (2026-10-23)
- Translations: each language section in TRANSLATIONS.md now starts with a one-line notice in that language saying it is a machine translation, not reviewed by a native speaker, and that the English version is authoritative. README Languages section notes this. No behavior changes.
- Local tests re-run and passed. Not tested in-app. Not submitted to the marketplace.

## 1.1.12 (2026-10-23)
- Search keywords: 33 to 40 (added CertificationPrep, VocationalTraining, CorporateTraining, GraduateSchool, workbooks, quizzes, SecondCheck); K12 written as k12 (single words lowercase, per Rob's keyword rules).
- Local tests re-run and passed. Not tested in-app. Not submitted to the marketplace.

## 1.1.11 (2026-10-22)
- Logo resized from 512x512 to 1024x1024 to match the rest of the plugin set (same artwork, no visual change). No behavior changes.

## 1.1.10 (2026-10-21)
- Added `tests/check_frontmatter.py`: a strict YAML front-matter check (PyYAML `safe_load`) for every SKILL.md and rules .mdc file, plus a plugin.json JSON check. Run `python3 tests/check_frontmatter.py` from the repo root; it catches the unquoted-colon bug fixed in PluginPulse 1.0.2.
- No behavior changes to skills or rules.

## 1.1.9 (2026-10-20)
- Example status labels updated after second checks (fresh text extraction from the original PDFs plus recalculation): Project Management items L6015, Table 12.4, Table 12.5, L6454, L6605 CONFIRMED; DaVinci L4947 and L3525 CONFIRMED, L5186 WITHDRAWN (not an error); TPW section 1.5 gap CONFIRMED (intent unknown).
- Sample report #6 (Rogers "10-page contract") CONFIRMED as a 14-page contract with a second source (The New York Times, 2006-10-25) alongside The Globe and Mail; export-example.json updated. #4 remains SINGLE-CHECK.
- Docs and examples only; no behavior changes.

## 1.1.8 (2026-10-20)
- TRANSLATIONS.md: each of the 23 languages now includes this plugin's specific limits list (from the README's "Honest assessment: what this plugin cannot do" section) plus the marketplace status. Machine translations, not reviewed by native speakers.
- Docs only; no behavior changes.

## 1.1.7 (2026-10-20)
- README follows the shared template: title, plain description, logo, existing content (Rob Domaine's four pillars unchanged), and a new final section "Honest assessment: what this plugin cannot do" listing real limits and the compliance statement.
- TRANSLATIONS.md now covers the same 23 languages as every Omnipotent plugin (title, description and honest-assessment summary for each), all marked as machine translations not reviewed by native speakers.
- Docs only; no behavior changes.

## 1.1.6 (2026-10-20)
- Multi-language: the rule file and every skill tell the AI to answer in the user's language, keep commands, file names and status labels unchanged, and quote and correct material in its own language. Added TRANSLATIONS.md with short summaries in 20 languages (machine-made, not yet reviewed by a native speaker).
- "No Google or Facebook services" reworded to "No Google or Facebook account is required" so it states the plugin's needs without blocking users' own sources.
- README: the description now sits at the top, under the logo.

## 1.1.5 (2026-10-15)
- Merged the two pillars sections in the rule file into one, in Rob Domaine's words and order; all earlier rules kept as sub-bullets.

## 1.1.4 (2026-10-15)
- Added README "Project status: done, pending, uncertain" section.
- Pillars restated in Rob Domaine's wording in the README and rule file.

## 1.1.3 (2026-10-15)
- Full re-test. Status labels in examples aligned to the defined set (UNCONFIRMED replaced by SINGLE-CHECK). Added a second real sample report (TLCL notes, HISTSIZE). Note on the older sample report format.

## 1.1.2 (2026-10-14)
- JSON and CSV export examples.

## 1.1.1 (2026-10-14)
- Clearer trigger description, README quick start, edge cases (huge documents, scanned PDFs, non-English, conflicting and paywalled sources), severity scoring, JSON and CSV export.

## 1.1.0 (2026-10-14)
- Scope covers all levels, fields and material types, including licensing and certification prep.
- Added field guide, Rob Domaine's four pillars as required steps, double-check statuses, licensing and high-stakes cautions, blind-spot checks.
- Added issue templates, a Feedback and reviews section and the new logo.
- Re-verified examples: 1 withdrawn (DaVinci +6 dB), 1 new error found (Challenger memo date), others marked UNCONFIRMED.

## 1.0.0 (2026-10-14)
- Added logo, credits, repository and homepage URLs. First public release.

## 0.1.0 (2026-10-14)
- First local build: audit-course-material, check-quiz-and-test, build-errata-sheet skills; source-integrity rule; worked examples.
