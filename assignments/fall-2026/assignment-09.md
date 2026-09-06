# Assignment 9 — Build-and-break replication

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 13: Try to defeat your own conclusion](../../lessons/13-limits-and-replication/README.md) and [Lesson 14: Build something worth auditing](../../lessons/14-build-and-break-studio/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record Will your strongest result survive a new held-out case, a different assumption, and a second implementation? Register separate expectations. Which two skeptical instruments are most likely to expose a weakness in your proposed build? Predict a measurable result for each. Preserve the original record and date any later revision.

## Build It

Build a Python replication runner that compares an initial implementation with a separately derived check over frozen cases. Track agreement, disagreement, unsupported scope, and cases where both methods may share an assumption.

Build a bounded Python artifact of your choice: dataset pipeline, classifier, prompt workflow, chart generator, or simulated agent. Implement two instruments from lessons 2–12 and define their input/output contracts before using them.

## Use It

Ask Claude to formulate the strongest counterargument to your report. Test the measurable part. Separate an observed failure, a theoretical assumption, and a philosophical claim of impossibility.

Use Claude Code to help implement, debug, and challenge the build. Maintain a record of accepted, changed, and rejected suggestions. Request a peer critique when available; honestly record if no peer participated.

## Ship It

Package replication-report.md, independent check, frozen cases, disagreement log, and revised scope statement; build-and-break-packet/ with runnable artifact, two audits, source credits, evidence, and a scope statement. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Include a planted shared-error case to show why agreement is insufficient. Repeat an earlier calibration task and compare your predictions with outcomes. Record actual findings even when the original claim survives.

Run the predeclared probes. Report a discovered defect or, if none was found, the tested boundary and residual uncertainty. Never invent a failure to satisfy a confession requirement.

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

