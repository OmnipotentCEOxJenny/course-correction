# Worked examples: real findings from Echo's course audits

These come from Echo's own study of free textbooks (October 2026). Line numbers (L) refer to Echo's saved text copy of each book.

## DaVinci Resolve training book (editing lessons)
| Location | Type | Severity | Original | Correction | Method | Confidence |
|---|---|---|---|---|---|---|
| L2309 vs L2503 | structure | high | A1 destination disabled at L2309; at L2503 the reader is told to place STORE 28 "with the audio" | Add a step to re-enable A1 before L2503 | Internal consistency check | high |
| L4947 | typo | medium | "5.5 dBFS" used for a gain change | "5.5 dB" (dBFS is an absolute level, not a gain amount) | Unit check | high |
| L4902 to L4906 | unclear | low | "+6 dB" in the text vs "3 dB" in the tooltip wording | Explain which value applies where | Internal consistency check | medium |
| L5186 | unclear | medium | Linked Selection "enable" wording where the action disables it | "Disable Linked Selection" | Internal consistency check | high |
| L3525 | typo | low | "WHITE SAND 36" | "WHITE SANDS 36" (clip name used elsewhere) | Internal consistency check | high |

## Project management textbook (Chapters 12 and 13)
| Location | Type | Severity | Original | Correction | Method | Confidence |
|---|---|---|---|---|---|---|
| Ch 12 text | math | medium | Total $661.25 | $661.65 (216.65 + 445) | Recomputed | high |
| Table 12.4 | math | medium | Small Boxes BCWS $7.00 | $17.00 | Recomputed from table rows | high |
| Table 12.5 | math | medium | SV shown without its sign | SV = -99.55 | Recomputed | high |
| Ch 12 summary | fact | medium | SV compares "spent so far (EV)" | EV is earned value; money spent is AC | Definition check within the book | high |
| Ch 13 text | structure | low | "Table 13.1 illustrates" cost-plus | Figure 13.2 | Cross-reference check | high |

## Technical writing textbook (TPW)
| Location | Type | Severity | Original | Correction | Method | Confidence |
|---|---|---|---|---|---|---|
| Section numbering | structure | medium | Section 1.5 is missing from the sequence | Flag the numbering gap to the publisher; confirm against the official edition | Numbering check | medium |
| Challenger case | fact | high | Engineers described as "MIT" | Morton Thiokol (MTI) | Echo course caveat; confirm against the Rogers Commission report (not re-opened for this example) | medium |
