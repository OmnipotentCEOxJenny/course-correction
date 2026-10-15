# Correction report: Echo's notes on The Linux Command Line (William Shotts, 25.12A), tlcl-notes.md line 7

Audited: 2026-10-15  Level and field: adult self-study, IT  Scope: one sentence  Auditor: Echo
Source versions: GNU Bash Reference Manual (gnu.org, fetched 2026-10-15); bash 5.2.37; Debian /etc/skel/.bashrc

| # | Location | Type | Severity | Original (exact) | Correction | Check 1 | Check 2 | Status | Confidence |
|---|----------|------|----------|------------------|------------|---------|---------|--------|------------|
| 1 | tlcl-notes.md L7 | unclear | low (score 2: impact 1 x reach 2) | "Up/down arrows recall command history (about 1,000 commands by default)." | "...(most distributions set 1,000; bash's own default is 500)." | Book L1015 to L1016: "Most Linux distributions remember the last 1,000 commands by default", so the note dropped the qualifier | GNU Bash manual, HISTSIZE: "The shell sets the default value to 500 after reading any startup files"; Debian /etc/skel/.bashrc sets HISTSIZE=1000 | CONFIRMED | high |

Result: the book is accurate as written; the error is in Echo's summary. No math in scope.
