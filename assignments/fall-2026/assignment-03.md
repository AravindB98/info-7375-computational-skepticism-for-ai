# Assignment 3 — Robustness and explanation

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 4: Break the shortcut you just built](../../lessons/04-robustness-and-shift/README.md) and [Lesson 5: A convincing explanation can explain the wrong thing](../../lessons/05-explanations-and-counterexamples/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record Which input changes should preserve the result, and which should change it? Name the distinction before designing probes. Will the feature named in a fluent explanation be necessary for the output? Predict a concrete removal test. Preserve the original record and date any later revision.

## Build It

Implement a deterministic Python probe runner recording baseline input, transformed input, expected relation, observed output, and pass/fail. Include whitespace or ordering invariance, a relevant semantic change, and a shifted slice.

Build an interpretable Python scoring rule with two or three features and a counterfactual enumerator over a small discrete input space. Report original score, changed feature, new score, decision change, and feasibility constraints.

## Use It

Ask Claude to critique your probe expectations and suggest a shortcut your implementation may exploit. Run at least three frozen probes on your own small classifier or prompt workflow. Keep live Claude observations separate from an offline surrogate.

Ask Claude to explain the rule from examples, then compare its narrative with executed feature changes. Test a correlated proxy and a feature with no effect. Label model sensitivity separately from real-world causation.

## Ship It

Package robustness-profile.csv, the baseline mechanism, probes, failures, and a residual-risk note; explanation-audit.md, scoring rule, counterfactual table, feasibility assumptions, and tests. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Use a known fragile baseline to establish that at least one probe can fail, then a targeted repair. Do not claim every perturbation preserves meaning. A passing finite suite is evidence only about those probes.

Compute at least two cases by hand. Test unchanged inputs, unreachable target decisions, and infeasible feature changes. A counterfactual of a program does not demonstrate an intervention on the world.

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

