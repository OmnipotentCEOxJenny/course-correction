# Worked examples: Echo's findings, re-verified 2026-10-14

High-severity items were re-checked twice (book text plus a second check). Others are marked UNCONFIRMED until re-checked. L = line in Echo's saved text copy of each book.

## DaVinci Resolve 20 Beginner's Guide
| Location | Type | Severity | Finding | Check 1 | Check 2 | Status |
|---|---|---|---|---|---|---|
| L2309 vs L2503 | structure | high | A1 destination is disabled at L2309 and never re-enabled, yet L2503 says "Press F12 to make a Place on Top edit, with the audio" | Book text L2309 to L2503 re-read: no re-enable step | Search of L2300 to L2510 for A1 or destination: only the disable step | CONFIRMED |
| L4947 | typo | medium | "around 5.5 dBFS" for a clip gain | | | UNCONFIRMED (likely dB; positive dBFS is not possible) |
| L5186 | unclear | low | "This will enable you to adjust..." read as wrong wording | | | UNCONFIRMED (downgraded: "enable" here means "allow") |
| L3525 | typo | low | "WHITE SAND 36"; clip is WHITE SANDS 36 everywhere else (L2265, L3073) | | | UNCONFIRMED |
| L4902 to L4913 | | | "+6 dB" vs "3 dB" listed as a conflict | Book: tooltip shows -3 dB, +6 dB adjustment brings it to about +3 dB | -3 + 6 = +3 | WITHDRAWN (the book is consistent) |

## Project Management, 2nd Edition (open textbook)
| Location | Type | Severity | Finding | Status |
|---|---|---|---|---|
| L6015 | math | medium | Total "$661.25"; 216.65 + 445.00 = 661.65 | UNCONFIRMED (book text matches; second check pending) |
| Table 12.4, L6217 | math | medium | Small Boxes BCWS "$7.00"; 10 x $1.70 = $17.00 (L5977, L6154) | UNCONFIRMED |
| Table 12.5, L6442 | math | medium | SV shown as "$99.55"; text gives ($99.55), negative | UNCONFIRMED |
| L6454 | fact | medium | SV is "the part of the budget that has been spent so far (EV)"; EV is earned value, spending is AC | UNCONFIRMED |
| L6605 | structure | low | "Table 13.1 illustrates" cost-plus; that is Figure 13.2 (L6703) | UNCONFIRMED |

## Technical and Professional Writing (TPW)
| Location | Type | Severity | Finding | Check 1 | Check 2 | Status |
|---|---|---|---|---|---|---|
| L933 to L955 | fact | high | Challenger engineers called "MIT engineer Roger Boisjoly" and "MIT's" | Rogers Commission report, Vol. 4 p. 691 (nasa.gov): "Interoffice Memo, Morton Thiokol, Inc.; From: R. Boisjoly to R.K. Lund" | Memo copy (Online Ethics Center): letterhead "Morton Thiokol, Inc, Wasatch Division" | CONFIRMED: Morton Thiokol (MTI) |
| L933 | fact | high | NEW: memo dated "July 22, 1985" | Rogers Commission Vol. 4 p. 691: "Dated: 31 July 1985" | Memo copy: "31 July 1985" | CONFIRMED: July 31, 1985 |
| Table of contents, L33 to L37 | structure | medium | Section 1.5 is missing (1.4 goes to 1.6) | | | UNCONFIRMED (the gap is in the TOC; whether it is intentional is not known) |
