# Lesson 15 — Ship a contribution another person can verify

**Predict → Build It → Use It → Ship It → Verify**

Reading: [accountability who is responsible when the system fails](../../chapters/12-accountability-who-is-responsible-when-the-system-fails.md) — The gate: the attestation you sign. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–14, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Can a new reader reproduce your headline result from the shipped version? Predict the likely point of failure. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Integrate the studio artifact into a coherent Python project with documented inputs, reproducible commands, tests, evidence, and an explicit decision boundary. Add one transfer case outside your development examples. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/15-capstone-and-transfer/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Use Claude to review the handoff README against actual files. The human chooses what is ready, what remains unsupported, and what may be shared. A professional contribution may be a rigorous bounded audit, not a deployed product. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver capstone-packet/ with README, code, tests, predictions, evidence, FRICTIONAL.md, CONTRIBUTIONS.md, and VERIFICATION.md. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Reproduce from a fresh directory with only declared inputs. Compare hashes and results. Record reviewer identity only for actual reviewers. If verification fails, revise and identify the newly submitted commit. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. What remains after the final verification?

<details>
<summary>Check your explanation after answering</summary>

A bounded conclusion and an accountable handoff, with unresolved limits still visible.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Irreducibly Human

[Reading map: metacognitive and supervisory work](../../docs/reading-map.md#irreducibly-human). Chapter 4's discussion of monitoring motivates comparing confidence with actual results.

**AI should** draft candidate code, calculate metrics, propose counterexamples, and help organize the evidence for this artifact.

**Human should** make the initial prediction, work through one calculation or case, choose the criterion that matters, inspect the evidence, and own the conclusion and authorized handoff. Record what you accepted, changed, rejected, or still do not understand in CONTRIBUTIONS.md. Do not invent a human review.

