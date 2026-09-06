# Assignment 4 — Bias and fairness

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 6: Find the decision that produced the disparity](../../lessons/06-bias-in-the-pipeline/README.md) and [Lesson 7: Choose the criterion before optimizing it](../../lessons/07-fairness-and-tradeoffs/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record At which pipeline step will the biggest group difference appear: sampling, labels, filtering, or thresholding? State an expected direction. Will one threshold make selection rates, TPR, and FPR equal across your two groups? Predict from the confusion counts. Preserve the original record and date any later revision.

## Build It

Implement a Python pipeline audit that records group counts and positive rates before and after each transformation. Use synthetic groups A and B. Make a deliberate biased filtering rule, then measure the effect of removing it.

Implement per-group confusion matrices, selection rate, TPR, FPR, and precision in Python. Report undefined denominators as null with a reason. Sweep a few thresholds and preserve the full tradeoff table.

## Use It

Ask Claude to generate alternative explanations for your observed gap. Draw the path from collection to action and identify which hypothesis your data can distinguish. Treat synthetic groups as teaching constructs, not real demographic findings.

Ask Claude to argue for two different fairness priorities in a fictional decision setting. Choose a priority and justify its costs and affected parties. Distinguish predictive parity (positive predictive value) from score calibration; the source manuscript sometimes conflates them.

## Ship It

Package pipeline-audit.csv, transformation code, an assumptions diagram, and an intervention comparison; fairness-choice.md, group metrics, threshold sweep, denominators, and monitoring proposal. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Preserve denominators at every step, test an empty group, and recompute one group rate by hand. Compare the proposed repair with a baseline on the same frozen rows.

Use unequal base rates and inspect tradeoffs on your own numbers. Also test identical groups and perfect predictions: do not assert a universal impossibility regardless of assumptions. A metric cannot choose the values objective.

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

