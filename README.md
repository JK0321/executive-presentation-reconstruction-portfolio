# Executive Presentation Reconstruction & Financial Validation

**[Explore the Interactive Portfolio](https://jk0321.github.io/executive-presentation-reconstruction-portfolio/)**

Downloads: [Northstar Cloud executive deck (PowerPoint)](deliverables/northstar_cloud/executive_revenue_review_v5.pptx) · [PDF](deliverables/northstar_cloud/executive_revenue_review_v5.pdf) · [Microsoft FY2026 Q4 calculated metrics (CSV)](data/microsoft_fy2026_q4_calculated_metrics.csv)

Portfolio proof of concept | Python · PowerPoint · Financial Analysis · Automated QA

An AI-assisted workflow for reconstructing editable PowerPoint presentations, validating financial information against primary sources, and redesigning decks for executive decisions.

**Case 01 — Northstar Cloud (synthetic data, fictional company):** a controlled business review taken from a weak four-slide deck to a decision-oriented executive presentation, with every number traced to source. Read the case: [case_01_northstar_cloud.md](case-studies/case_01_northstar_cloud.md).

**Case 02 — Microsoft FY2026 Q4 (public financial disclosures):** a real-world exercise: slide figures checked against the official financial statements, seven slides rebuilt blind from images, and every result measured with documented methods. Slides derived from Microsoft material are not published here. Read the case: [case_02_microsoft_fy2026_q4.md](case-studies/case_02_microsoft_fy2026_q4.md).

## Validation results (private working repository, 14 October 2026)

| Check | Result |
|---|---|
| Automated pipeline, full run with private source files | 16 of 16 steps passed |
| Unit tests | 82 passed |
| Microsoft slide values against the official financial statements | 85 of 85 match |
| Reconstruction text against an internally checked reference transcription | 7 of 7 slides match |
| OCR text-agreement test (threshold 0.98) | FAIL on 3 of 7 slides — retained; the OCR tool cannot reach 0.98 even on known text. [Detailed explanation](https://jk0321.github.io/executive-presentation-reconstruction-portfolio/#ocr-test) |
| Independent review | NOT TESTED |
| Hands-on accessibility testing | NOT TESTED |

Public visitors cannot rerun the automation or the tests: they are kept in the private working repository. The results above are reported as recorded on the date shown.

Methods, financial verification, technical decisions, QA results, and limits: [EVIDENCE.md](EVIDENCE.md).

## Project scope

This is an independently developed, AI-assisted portfolio demonstration. It was not commissioned, sponsored, reviewed, or endorsed by Microsoft. "Microsoft" is a trademark of Microsoft Corporation. Source: Microsoft FY2026 Q4 earnings release, <https://www.microsoft.com/en-us/investor/earnings/fy-2026-q4/press-release-webcast>.

The project demonstrates analytical direction, workflow design, financial verification, quality assurance, and documented decision-making. Implementation was performed with AI coding assistance. The automation and tests are kept private; results are reported as recorded.
