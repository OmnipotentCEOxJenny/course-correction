# Course Correction

![Course Correction logo](assets/logo.png)

## Credits
- Inventor and publisher: Rob Domaine / Omnipotent Media LLC
- Builder: Jenny Echo

License: MIT. Free to use.

Repository and homepage: https://github.com/OmnipotentCEOxJenny/course-correction

Course Correction has an AI review courses, tests, quizzes, workbooks, answer keys and study guides at every level (K-12, college and graduate, vocational and trade, corporate training, licensing and certification prep such as FINRA SIE and Series 7, 63, 65, 66, CPA, bar, NCLEX, IT, real estate and insurance), in every field. It finds mistakes (wrong facts, math slips, outdated claims, unclear passages, typos), corrects them with sources, and produces a cleaner version so the next student learns from better material.

## Quick start
1. Install (see Installation).
2. Give the agent a file: "Audit chapter 3 of this textbook with Course Correction."
3. Get a correction report (two checks per fix), a corrected version, and optional JSON or CSV export.

## Rob Domaine's four pillars
Created by Rob Domaine and required in every audit:
1. Truth always: never invent; unverifiable means UNVERIFIED.
2. Double-check: every correction is confirmed twice, and the report shows both checks.
3. Obey laws and platform rules: copyright and fair use, exam confidentiality, publisher terms.
4. Only legitimate, proven sources: primary and authoritative first; unreliable sources rejected.

## Cautions
- No copyrighted or confidential exam questions or proprietary prep material are reproduced. It audits what you supply.
- Medical, legal and financial output is a review aid, not professional advice; flags need expert confirmation.
- Rules and figures change: it checks the current version and date.

## Components
- `skills/audit-course-material`: the core audit. Extracts claims, figures and calculations; checks facts against primary sources; recomputes math; flags outdated material; classifies each issue by type and severity; writes a correction report (original, correction, source, confidence) and an improved version.
- `skills/check-quiz-and-test`: checks quizzes, tests and answer keys against the material.
- `skills/build-errata-sheet`: turns correction reports into a one-page errata sheet.
- `rules/source-integrity.mdc`: the four pillars, plus checks for student privacy, accessibility, bias and non-English material.
- `skills/audit-course-material/references/field-guide.md`: what to check in each field and which authoritative sources to use.
- `examples/`: real findings and a full sample report.

## Requirements
No paid APIs. No Google or Facebook services. Uses only the agent's normal file reading and free public web sources.

## Installation
Copy this folder to `~/.cursor/plugins/local/course-correction/`, or install from the marketplace once listed.

## Usage
Ask: "Audit chapter 3 of this textbook with Course Correction" and supply the file.


## How it started

Course Correction came out of real study. Jenny Echo, an AI assistant working for Rob Domaine, was working through textbooks and courses one by one, taking notes, doing the exercises and sitting closed-book tests graded against each book. Learning the material deeply is what made the mistakes visible. A settlement figure didn't match the court record. A step that turned audio off never turned it back on. A memo date and an engineer's employer didn't match the official commission report. A section number was missing from the table of contents. Each time, checking the book against primary sources showed that the book itself was wrong, not the student.

Rob saw the pattern and had the idea: if studying closely teaches you to notice mistakes, an AI can do that review on purpose for every course, so the next student learns from a cleaner version. Every check in this plugin follows Rob's four pillars: truth first, double-check everything, obey the law and platform rules, and use only legitimate sources.

## Feedback and reviews
- Reviews and general feedback: [Discussions](https://github.com/OmnipotentCEOxJenny/course-correction/discussions)
- Report a wrong correction: [open an issue](https://github.com/OmnipotentCEOxJenny/course-correction/issues/new?template=wrong-correction.md)
- Feature request: [open an issue](https://github.com/OmnipotentCEOxJenny/course-correction/issues/new?template=feature-request.md)
