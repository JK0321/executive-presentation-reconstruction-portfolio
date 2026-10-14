# Evidence Summary

**Profile:** reference. **Readers:** visitors who want to check how the portfolio results were produced. **Purpose:** a curated summary of the methods, the financial verification, the main technical decisions, the QA results and limits, and who did what.

All results were recorded in the private working repository on 14 October 2026. The automation and the tests are not published, so visitors cannot rerun them.

## 1. Reconstruction methodology
**Case 01 (Northstar Cloud).** The original deck is an editable PowerPoint file. It was rebuilt from a declared specification and compared with the original property by property and pixel by pixel: 596 properties compared, 0 material differences, 0.0000 % changed pixels on 4 of 4 slides.

**Case 02 (Microsoft FY2026 Q4).** The original deck is image-only: every slide is one picture. Seven of its 23 slides were rebuilt blind:
1. The seven slides were rendered to images. The original files were then locked by an operating-system access rule.
2. A separate AI agent with no access to the original files rebuilt the slides from the images only, as native text boxes, tables, and a chart.
3. An audit after the run checked the boundary (7 of 7 checks passed). Limits: the folder owner could change the access rule, and network access was forbidden by instruction, not blocked.
4. Later correction rounds (not blind) fixed defects found by measurement: underline width, type size and weight, line wraps, footnote spacing, a text box past the slide edge, and rule shadow and weight. Each fix was re-rendered and re-measured.

Measured result: 0 pictures (4 native tables, 1 native chart); median text-line position offset 0.06 % to 0.17 % of the slide; median text-height ratio 0.984 to 1.023. Accepted differences: the cover typeface (the source face is not installed), square instead of rounded bar tops (a chart-tool limit), and no slide titles or picture descriptions (the images do not show them).

## 2. Financial verification
**Case 01.** The synthetic data passed 12 of 14 data checks; 2 cannot be tested with the data supplied (no segment or component data). Every number on the executive deck (98 figures and chart points) is produced by one calculation engine and traced to a source cell or a documented calculation. One figure is derived (implied gross profit) and its assumption is on the slide.

**Case 02.** Six official files were downloaded from Microsoft's investor-relations site and recorded with their SHA-256 checksums. Then:
- 15 of 15 statement ties hold (for example revenue − cost of revenue = gross margin; segments sum to the total).
- 85 of 85 slide values match the official statements after rounding to the precision shown (one is consistent only within rounding: a 70 % growth figure computed from inputs disclosed to USD 0.1 billion).
- 67 metrics were calculated independently (growth = current / prior − 1; margin = item / revenue; point changes from unrounded margins; half-up rounding to the shown precision).
- 5 of 5 press-release sentences were rebuilt from the statements.

## 3. Significant technical decisions
| Decision | Reason |
|---|---|
| Keep the faithful reconstruction separate from the executive redesign | A polished redesign is not proof of a faithful copy |
| Build every slide from editable PowerPoint objects; no pictures of text | Editability and accessibility |
| Produce every slide number from one calculation engine and check the slide text against a claims register | A number typed by hand cannot pass the check |
| Use zero-based axes; show the case-01 gross-profit bridge as a zero-based waterfall | Avoid exaggerating differences; the small steps are labelled instead |
| State rank, not prediction ("lowest of the seven metrics") | The data supports a rank only |
| Keep acceptance thresholds fixed; report a failed test as failed | Results must not be tuned to pass |
| Measure the measuring tool: an OCR self-check on known text | Separate instrument error from reconstruction error |
| Add a second text measure that needs no OCR on the rebuild, against an internally checked reference transcription | The OCR could not decide the threshold on five slides |
| Keep Microsoft-derived slides and the original files out of the public portfolio | No redistribution license; independence |

## 4. QA results and known limitations
| Check | Result |
|---|---|
| Automated pipeline, full run with private source files | 16 of 16 steps passed |
| Unit tests | 82 passed |
| Case 02: slide values against the official statements | 85 of 85 |
| Case 02: reconstruction text against an internally checked reference transcription | 7 of 7 slides match |
| Case 02: OCR text-agreement test (threshold 0.98) | FAIL on 3 of 7 slides (0.978, 0.969, 0.976), retained. On known text the OCR reaches only 0.957 to 0.974 on 5 slides |
| Automated accessibility checks (text size, contrast, slide titles, reading-order start, chart and table descriptions, document title and language) | Passed on both executive decks |
| PowerPoint Accessibility Checker and screen-reader test | NOT TESTED |
| Independent review | NOT TESTED |

**How the internally checked reference was made.** The OCR text of the original slides was corrected in 43 documented places where the OCR misread or missed a token. Each correction is backed by an image crop of the original, inspected internally. An independent reviewer has not checked these corrections.

**Other limits.** Case 01 uses synthetic data, so the business records behind it cannot be verified. Only 7 of the 23 Microsoft slides were rebuilt. The automated accessibility checks do not replace hands-on testing.

## 5. Human direction and AI-assisted implementation
- **Human direction (the portfolio owner):** set the objectives, scope, requirements, and acceptance standards; chose the two cases; made the decisions on scope, privacy, and publication; and approved the public text.
- **AI-assisted implementation:** an AI coding assistant (Claude, by Anthropic) wrote the code and the tests, ran the pipeline, carried out the internal inspections, and drafted the analyses and documents under the owner's direction. The blind reconstruction was done by a separate AI agent instance with restricted access.
- **Review:** all internal checks were done by automated tests or by the AI assistant. No independent human reviewer has checked the work yet.
