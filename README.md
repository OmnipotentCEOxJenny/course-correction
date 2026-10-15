# Course Correction

![Course Correction logo](assets/logo.png)

## Credits
- Inventor and publisher: Rob Domaine / Omnipotent Media LLC
- Builder: Jenny Echo

License: MIT. Free to use.

Repository and homepage: https://github.com/OmnipotentCEOxJenny/course-correction

Course Correction has an AI review existing courses, classes and textbooks. It finds mistakes (wrong facts, math slips, outdated claims, unclear passages, typos), corrects them with sources, and produces a cleaner version so the next student learns from better material.

## Components
- `skills/audit-course-material`: the core audit. Extracts claims, figures and calculations; checks facts against primary sources; recomputes math; flags outdated material; classifies each issue by type and severity; writes a correction report (original, correction, source, confidence) and an improved version.
- `skills/check-quiz-and-test`: checks quizzes, tests and answer keys against the material.
- `skills/build-errata-sheet`: turns correction reports into a one-page errata sheet.
- `rules/source-integrity.mdc`: never invent sources; mark unverifiable claims; free sources only.
- `examples/`: real findings and a full sample report.

## Requirements
No paid APIs. No Google or Facebook services. Uses only the agent's normal file reading and free public web sources.

## Installation
Copy this folder to `~/.cursor/plugins/local/course-correction/`, or install from the marketplace once listed.

## Usage
Ask: "Audit chapter 3 of this textbook with Course Correction" and supply the file.
