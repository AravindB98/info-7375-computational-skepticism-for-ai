# Assignment 7 — Visualization and uncertainty

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 10: One dataset, two stories](../../lessons/10-visualization-under-validation/README.md) and [Lesson 11: Make the sentence no stronger than the evidence](../../lessons/11-uncertainty-and-claims/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record How will changing the axis baseline alter perceived improvement without changing a single value? Sketch both views first. Which sentence in your report makes the largest unsupported leap? Predict what would force you to weaken it. Preserve the original record and date any later revision.

## Build It

Use Python to produce two SVG bar charts from the same small CSV: one starting at zero and one clearly labeled truncated-axis demonstration. Print values, units, sample size, and transformation choices alongside them.

Implement a Python claim-evidence linter that flags strong verbs and absent evidence references. Preserve its output as review suggestions, not automatic truth judgments. Add a claim table naming scope, evidence, uncertainty, and a possible defeater.

## Use It

Ask Claude to critique the message each chart conveys. Make an honest final chart for a named reader, including relevant uncertainty or a clear statement that the dataset cannot estimate it.

Ask Claude to rewrite one result for a general reader and a technical reviewer. Audit each version against the original data, then revise the claim yourself and state what would change your mind.

## Ship It

Package chart-comparison.md, both labeled teaching SVGs, source CSV, generation script, and final chart; three-layer-report.md, claim table, linter, flagged examples, and revision diff. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Verify bar geometry against source numbers and labels. Test equal values, zero range, and negative inputs according to your documented chart contract. Ship the misleading demonstration only with its explanatory comparison.

Test a quotation, negation, and a fully supported claim containing a flagged word. Record false positives and false negatives. Check one number from the report against raw output.

Reproduce using only declared inputs. Record the actual result, limitations, and any revised commit. No invented failures, struggle, approvals, or live runs.

## Rubric — 100 points

| Implementation criterion | Points | Full-credit evidence |
|---|---:|---|
| Prediction and acceptance contract | 8 | Specific original expectations, assumptions, and a measurable failure condition. A wrong prediction alone does not lose credit. |
| Python implementation | 22 | Working requested mechanisms with documented inputs, outputs, and meaningful boundaries. |
| Applied use and evidence | 12 | Actual application to the stated task, preserved outputs, and explicit fixture/live distinctions. |
| Verification | 12 | The specified hand checks and failure cases, reproduction of the shipped version, and candid limits. |
| Technical handoff and explanation | 6 | Explainable mechanisms, reproducible commands, credited sources, and a conclusion supported by the evidence. |
| **Implementation subtotal** | **60** | |
| [Frictional](../../prerequisites/frictional.md) | 10 | Honest effort and learning log. |
| [GitHub posting](../../prerequisites/github-submission.md) | 10 | Correctly delivered, identifiable version matching Canvas. |
| [Relative Quartile](../../prerequisites/relative-quartile.md) | 20 | Overall quality relative to peers after all submissions are reviewed. |
| **Total** | **100** | |

For implementation rows, award full points for complete evidence, proportionate partial credit for a documented partial implementation, and zero when the required evidence is absent. Explain deductions. The technical handoff row assesses usability and understanding; GitHub points assess delivery. Frictional assesses the actual process, not whether the result succeeded. A finding that survives the audit can earn full credit when checks are discriminating and scope is honest.

An explainer video or Brutalist production is optional and may support communication quality within Relative Quartile. It has no separate points; excellent written evidence can earn full credit. Claude Code is assumed; direct API calls and paid media tools are unnecessary.

