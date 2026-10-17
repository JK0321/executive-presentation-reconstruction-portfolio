# Executive Presentation Reconstruction & Financial Validation

**[Explore the Interactive Portfolio](https://jk0321.github.io/executive-presentation-reconstruction-portfolio/)**

Downloads: Northstar Cloud deck v6, [presenter deck (PowerPoint)](deliverables/northstar_cloud/executive_revenue_review_v6.pptx) · [leave-behind (PowerPoint)](deliverables/northstar_cloud/executive_revenue_review_v6_leave_behind.pptx) · [Microsoft FY2026 Q4 calculated metrics (CSV)](data/microsoft_fy2026_q4_calculated_metrics.csv)

Portfolio proof of concept | Python · PowerPoint · Financial Analysis · Automated QA

An AI-assisted workflow for reconstructing editable PowerPoint presentations, validating financial information against primary sources, and redesigning decks for executive decisions.

**Case 01 — Northstar Cloud (synthetic data, fictional company):** a controlled business review taken from a weak four-slide deck to a decision-oriented executive presentation, with every number traced to source. Version 6 is a 9-slide presenter deck and a 10-slide standalone leave-behind; version 5 is kept as the previous version. Read the case: [case_01_northstar_cloud.md](case-studies/case_01_northstar_cloud.md).

**Case 02 — Microsoft FY2026 Q4 (public financial disclosures):** a real-world exercise: slide figures checked against the official financial statements, seven slides rebuilt blind from images, and every result measured with documented methods. Slides derived from Microsoft material are not published here; the redesign is described in text only. Read the case: [case_02_microsoft_fy2026_q4.md](case-studies/case_02_microsoft_fy2026_q4.md).

A third case study is kept private; it can be shown on request.

## Working standard for sales presentations
The project uses its own draft Sales Presentation Engineering Standard as its working gold standard for presentations. Its status is DRAFT / NOT CERTIFIED. It is a working method, not a certification, and no deck is claimed to conform to it. In practice it asks for:
- assertion titles that state a conclusion the evidence supports;
- the answer and the decision requested first;
- an evidence register: every figure traced to a source cell or a calculation;
- two delivery modes: a presenter deck and a standalone leave-behind;
- no slide without evidence: a missing step is omitted and listed with its reason on the data-notes slide;
- stage gates and tests, each reported as an automated check, an internal review, or NOT TESTED.

## Version history
| Date | Change |
|---|---|
| 17 October 2026 | Case 01 deck v6 (presenter deck and leave-behind, PDFs, slide renders, claims register, before-and-after images) becomes the public version. Deck v5 moves to the previous-versions folder. Case 02 redesign v2 is described in text. |
| 14 October 2026 | First public release: Case 01 deck v5, Case 02 results and calculated metrics. |

## Validation results (private working repository, 14 October 2026)

| Check | Result |
|---|---|
| Automated pipeline, full run with private source files | 16 of 16 steps passed |
| Unit tests | 82 passed on 14 October 2026; more than 200 passed on 17 October 2026 |
| Microsoft slide values against the official financial statements | 85 of 85 match |
| Reconstruction text against an internally checked reference transcription | 7 of 7 slides match |
| OCR text-agreement test (threshold 0.98) | FAIL on 3 of 7 slides — retained; the OCR tool cannot reach 0.98 even on known text. [Detailed explanation](https://jk0321.github.io/executive-presentation-reconstruction-portfolio/#ocr-test) |
| Independent review | NOT TESTED |
| Hands-on accessibility testing | NOT TESTED |

**Update, 17 October 2026 (Case 01 v6 and Case 02 v2).** Case 01 v6: 96 of 96 figures traced in each mode; automated deck checks 100 pass (presenter) and 110 pass (leave-behind), 0 fail. Case 02 v2: all 117 figures of the first redesign are traced in v2, plus one declared addition. The OCR result above stays FAIL. All checks are automated checks or internal reviews, including reviews by AI models. The PowerPoint Accessibility Checker, a screen-reader test, an independent comprehension test, and independent human review are NOT TESTED. Reviewer scores are NOT ASSESSED.

Public visitors cannot rerun the automation or the tests: they are kept in the private working repository. The results above are reported as recorded on the date shown.

Methods, financial verification, technical decisions, QA results, and limits: [EVIDENCE.md](EVIDENCE.md).

## Project scope

This is an independently developed, AI-assisted portfolio demonstration. It was not commissioned, sponsored, reviewed, or endorsed by Microsoft. "Microsoft" is a trademark of Microsoft Corporation. Source: Microsoft FY2026 Q4 earnings release, <https://www.microsoft.com/en-us/investor/earnings/fy-2026-q4/press-release-webcast>.

The project demonstrates analytical direction, workflow design, financial verification, quality assurance, and documented decision-making. Implementation was performed with AI coding assistance. The automation and tests are kept private; results are reported as recorded.
