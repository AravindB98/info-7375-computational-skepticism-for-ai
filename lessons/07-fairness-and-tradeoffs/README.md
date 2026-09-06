# Lesson 7 — Choose the criterion before optimizing it

**Predict → Build It → Use It → Ship It → Verify**

Reading: [fairness metrics choosing a definition and defending it](../../chapters/07-fairness-metrics-choosing-a-definition-and-defending-it.md) — Three definitions. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–6, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Will one threshold make selection rates, TPR, and FPR equal across your two groups? Predict from the confusion counts. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement per-group confusion matrices, selection rate, TPR, FPR, and precision in Python. Report undefined denominators as null with a reason. Sweep a few thresholds and preserve the full tradeoff table. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/07-fairness-and-tradeoffs/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to argue for two different fairness priorities in a fictional decision setting. Choose a priority and justify its costs and affected parties. Distinguish predictive parity (positive predictive value) from score calibration; the source manuscript sometimes conflates them. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver fairness-choice.md, group metrics, threshold sweep, denominators, and monitoring proposal. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Use unequal base rates and inspect tradeoffs on your own numbers. Also test identical groups and perfect predictions: do not assert a universal impossibility regardless of assumptions. A metric cannot choose the values objective. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Who decides which error tradeoff is acceptable?

<details>
<summary>Check your explanation after answering</summary>

An authorized decision maker accountable to the affected context; the metric describes a consequence.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Irreducibly Human

[Reading map: metacognitive and supervisory work](../../docs/reading-map.md#irreducibly-human). Chapter 4's discussion of monitoring motivates comparing confidence with actual results.

**AI should** draft candidate code, calculate metrics, propose counterexamples, and help organize the evidence for this artifact.

**Human should** make the initial prediction, work through one calculation or case, choose the criterion that matters, inspect the evidence, and own the conclusion and authorized handoff. Record what you accepted, changed, rejected, or still do not understand in CONTRIBUTIONS.md. Do not invent a human review.

