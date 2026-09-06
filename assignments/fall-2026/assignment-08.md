# Assignment 8 — Accountability gate

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 12: An approval belongs to a particular action](../../lessons/12-accountability-and-gates/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record If a target changes after approval, should the approval still permit execution? Specify the rule before implementing it. Preserve the original record and date any later revision.

## Build It

Implement a Python proposal fingerprint over canonical JSON and bind an approval record to that fingerprint. Record owner, scope, evidence, decision, and expiration. Use a fixed injected clock in tests.

## Use It

Ask Claude to identify gaps in the approval packet for your existing workflow. Have a person make the classroom review decision or label a simulated decision. Do not connect this teaching gate to real consequential systems.

## Ship It

Package approval-packet.json, fingerprint implementation, expiry tests, changed-target test, and responsibility map. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Test changed target, changed effect, absent approval, expired approval, and matching approval. Explain that a hash alone does not authenticate a signer or secure a production system.

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

