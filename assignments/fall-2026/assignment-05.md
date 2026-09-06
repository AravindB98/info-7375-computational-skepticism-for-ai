# Assignment 5 — Agent outcome audit

**Fall 2026 · INFO 7375 · 100 points · Due: Canvas**

[AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz)

**Predict → Build It → Use It → Ship It → Verify**

Complete [Lesson 8: The agent said done. Check the state.](../../lessons/08-agent-outcomes-and-traces/README.md). These lesson Assessments are ungraded practice; submit one coherent version of their work here.

## Predict

Before the runs, record Will an agent transcript saying success correspond to the intended final state in every fixture? Identify a failure predicate first. Preserve the original record and date any later revision.

## Build It

Build a Python state-machine simulator with allowed actions, bounded steps, action-result logs, and a separate final-state checker. Include a success message whose underlying state remains unchanged.

## Use It

Ask Claude Code to propose action sequences against your local simulator. Run the sequences with no external accounts or consequential tools. Record transcript, tool result, and final state as separate evidence types.

## Ship It

Package agent-trace.json, simulator, outcome checks, success and failure fixtures, and diagnosis. Credit the source chapters, reference code, collaborators, and Claude's contributions. Add README.md, PREDICTIONS.md, CONTRIBUTIONS.md, FRICTIONAL.md, and VERIFICATION.md. Submit the final checked revision to Canvas and GitHub.

## Verify

Test genuine completion, falsely narrated completion, unauthorized action, and exhausted budget. Let the outcome checker reject a plausible success transcript. This is a simulator, not a live incident reproduction.

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

