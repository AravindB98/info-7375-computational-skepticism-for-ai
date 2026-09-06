# Lesson 11 — Make the sentence no stronger than the evidence

**Predict → Build It → Use It → Ship It → Verify**

Reading: [communicating uncertainty calibrating claims to evidence](../../chapters/11-communicating-uncertainty-calibrating-claims-to-evidence.md) — The verb taxonomy. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–10, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Which sentence in your report makes the largest unsupported leap? Predict what would force you to weaken it. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement a Python claim-evidence linter that flags strong verbs and absent evidence references. Preserve its output as review suggestions, not automatic truth judgments. Add a claim table naming scope, evidence, uncertainty, and a possible defeater. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/11-uncertainty-and-claims/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to rewrite one result for a general reader and a technical reviewer. Audit each version against the original data, then revise the claim yourself and state what would change your mind. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver three-layer-report.md, claim table, linter, flagged examples, and revision diff. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Test a quotation, negation, and a fully supported claim containing a flagged word. Record false positives and false negatives. Check one number from the report against raw output. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Can replacing proves with suggests repair a false numerical statement?

<details>
<summary>Check your explanation after answering</summary>

No. Rhetorical caution cannot replace checking the underlying claim.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Irreducibly Human

[Reading map: metacognitive and supervisory work](../../docs/reading-map.md#irreducibly-human). Chapter 4's discussion of monitoring motivates comparing confidence with actual results.

**AI should** draft candidate code, calculate metrics, propose counterexamples, and help organize the evidence for this artifact.

**Human should** make the initial prediction, work through one calculation or case, choose the criterion that matters, inspect the evidence, and own the conclusion and authorized handoff. Record what you accepted, changed, rejected, or still do not understand in CONTRIBUTIONS.md. Do not invent a human review.

