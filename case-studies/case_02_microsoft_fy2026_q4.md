# Case 02 — Microsoft FY2026 Q4 Earnings Presentation

**Independence.** This is an independent portfolio project based on Microsoft's public investor-relations files. It was not commissioned, reviewed, or endorsed by Microsoft. "Microsoft" and its product names are trademarks of Microsoft Corporation.

## Official sources
Microsoft Corporation, FY2026 Q4 earnings release, published 2026-07-29: <https://www.microsoft.com/en-us/investor/earnings/fy-2026-q4/press-release-webcast>. The case used six files from that page (earnings slides, financial statements workbook, press release, call transcript, outlook slides, Form 10-K), retrieved on 2026-10-13 (UTC). Their SHA-256 checksums are recorded in the project. The files themselves are not redistributed.

## The business problem
An earnings presentation is read quickly by executives and investors. Two questions matter before its design: are the numbers on the slides the numbers in the official statements, and does the deck lead the reader to the result and its drivers?

## The assignment
Verify the slide figures against the official statements; rebuild seven representative slides blind, from images only, as editable PowerPoint; review the original for genuine issues without inventing weaknesses; and design an executive version that puts the result first.

## Method
1. Record the official files with URLs, dates, and checksums.
2. Tie the statements (for example: revenue − cost of revenue = gross margin; segments sum to the total) and recompute growth rates and margins independently.
3. Render seven slides to images and lock the original files away. A separate agent with no access to the originals rebuilds the slides from the images; an audit checks the boundary.
4. Measure the rebuild: layout position, type size, editability, and text. Text is measured two ways and reported separately: OCR agreement, and the rebuild's own text against an internally checked reference transcription of the original.
5. Build the executive redesign from registered figures only, and run automated checks and an internal visual review.

## Independently derived results
All values were calculated in this project from the official statements (three months ended June 30, 2026, against the same quarter of 2025). They are listed with their formulas in [calculated_metrics.csv](../data/microsoft_fy2026_q4_calculated_metrics.csv).

| Measure | Result |
|---|---|
| Revenue growth | 17.7 % |
| Intelligent Cloud share of the revenue added | 69.5 % (USD 9,428 M of USD 13,566 M) |
| Gross margin percentage | 67.2 %, down 1.4 points |
| Operating margin | 45.1 %, up 0.2 points |
| Operating expense growth | 9.8 % |
| Net income growth (GAAP) | 31.3 % |
| Free cash flow change | −23.2 % (USD 19,639 M vs USD 25,568 M) |

## Verification results
| Check | Result | Evidence level |
|---|---|---|
| Source checksums | 6 of 6 verified | automated |
| Statement ties | 15 of 15 hold | automated |
| Slide values against the official statements | 85 of 85 match within the rounding shown | automated |
| Redesign figures traced to an official cell or formula | 117 of 117 | automated |
| Rebuild editability | 100 % native text, tables, and chart; 0 pictures (the original slides are single pictures) | automated |
| Rebuild layout | median text position offset 0.06 % to 0.17 % of the slide | automated |
| Rebuild text, OCR agreement (threshold 0.98) | FAIL on 3 of 7 slides. A self-check shows the OCR cannot reach 0.98 on 5 slides even on known text. | automated |
| Rebuild text against an internally checked reference transcription | 7 of 7 slides: F1 1.000, 0 unexplained differences | automated comparison; reference corrections checked by inspection |
| Every flagged text mismatch | 0 genuine text errors; all OCR errors | internal inspection |
| Independent review | not done | — |

## What the review found in the original
The original is a professionally produced deck, and its numbers are right: no figure needs correction. The main issues are about access and reuse. Every slide is a single picture, so the text cannot be searched, copied, or read by a screen reader, and the machine-generated picture descriptions omit most figures (one misstates the period). Two minor factual issues were found: one slide repeats the page number of another, and the cover uses a different typeface from the rest of the deck. The other findings are design choices, for example topic titles instead of conclusions, and segment growth shown as rates without each segment's dollar contribution (Intelligent Cloud added 69.5 % of the revenue increase). The redesign keeps what works (the consistent footnotes, the zero-based segment chart, GAAP and constant-currency growth side by side, the trend tables, and the reconciliation appendix) and adds a result-first summary and explicit drivers.

## Redesign v2 (described, not published)
Version 2 applies the project's draft Sales Presentation Engineering Standard (DRAFT / NOT CERTIFIED; no conformance claimed). It has two delivery modes: a 10-slide presenter deck and an 11-slide standalone leave-behind with a reading guide first.

| Check (17 October 2026) | Result | Evidence level |
|---|---|---|
| Figures of the first redesign traced in v2 | 117 of 117, plus 1 declared addition in the opening title | automated |
| Automated deck checks, presenter deck | 110 pass, 0 fail | automated |
| Automated deck checks, leave-behind | 120 pass, 0 fail | automated |
| Rebuild text against the internally checked reference transcription (unchanged) | 7 of 7 slides: F1 1.000 | automated comparison |
| Rebuild text, OCR agreement (threshold 0.98) | FAIL on 3 of 7 slides, kept as recorded; not rerun for v2 | automated |

A new decision slide asks the reader to agree which of three open questions to take to management. It gives no investment advice. The data-notes slide lists the omitted steps (market insight, future state as a scope choice, business case) and why. The v2 decks are not published because they present Microsoft material.

## Limits
- The executive redesign and the rebuilt slides are not shown here: they reproduce or present Microsoft material, and publishing them needs a separate decision.
- The reference transcription for the text check depends on documented internal corrections; an independent reviewer has not yet checked them.
- Accessibility was checked by script only; the PowerPoint Accessibility Checker and a screen-reader test have not been run.
- No independent comprehension test or independent human review has been done. Reviewer scores are NOT ASSESSED.

## Capabilities demonstrated
Financial verification against primary sources; independent recalculation with stated formulas and rounding; blind image-to-PowerPoint reconstruction under an access boundary; measurement design that separates instrument error from reconstruction error; transparent status reporting.
