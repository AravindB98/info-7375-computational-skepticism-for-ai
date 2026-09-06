# Assignment 1 — Claims and calibration

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 1: A claim you can try to break](../../lessons/01-skeptics-toolkit/README.md) and [Lesson 2: Confidence has to earn its number](../../lessons/02-probability-and-calibration/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record Which of three plausible claims will survive a check against its source? Write a confidence estimate and a possible falsifier for each. Will two predictors with identical threshold accuracy receive the same Brier score? Calculate one four-row example before running it. Preserve the original record and date any later revision.

## Build It

Implement a Python claim ledger: claim ID, exact claim, source path, observation, check method, status, and remaining uncertainty. Reject missing IDs, duplicate IDs, and unknown statuses. A status of supported must point to evidence; it must not be inferred from fluency.

Implement mean squared probability error in Python: average (p-y)^2. Validate nonempty equal-length inputs, finite probabilities in [0,1], and binary labels. Add reliability bins with counts and an explicit convention for p=1.

## Use It

Give Claude Code a small local source packet and ask for three claims with source locations. Choose and check the claims yourself, then ask Claude to propose a counterexample. Record which source actually supports each claim.

Ask Claude to suggest contrasting confidence vectors for the same labels. Freeze those vectors before scoring. Separate invented teaching probabilities from measured Claude confidence; verbal confidence is not a calibrated probability.

## Ship It

Package claim-ledger.json, your original predictions, a source packet, tests, and a short verdict; calibration-report.md, probability rows, reliability-bin counts, Python implementation, and tests. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Use one supported, one contradicted, and one unresolved synthetic example. Manually trace each status. A missing source must produce unresolved, never supported.

Check p=[0.9,0.8,0.4,0.1], y=[1,0,1,0] by hand: Brier=0.255. Compare with constant p=0.5, Brier=0.25. Test empty input, NaN, endpoints, and invalid labels.

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

