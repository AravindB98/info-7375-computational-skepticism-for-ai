# Lesson 2 — Confidence has to earn its number

**Predict → Build It → Use It → Ship It → Verify**

Reading: [probability uncertainty and the confidence illusion](../../chapters/02-probability-uncertainty-and-the-confidence-illusion.md) — chapter reading. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–1, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Will two predictors with identical threshold accuracy receive the same Brier score? Calculate one four-row example before running it. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement mean squared probability error in Python: average (p-y)^2. Validate nonempty equal-length inputs, finite probabilities in [0,1], and binary labels. Add reliability bins with counts and an explicit convention for p=1. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/02-probability-and-calibration/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to suggest contrasting confidence vectors for the same labels. Freeze those vectors before scoring. Separate invented teaching probabilities from measured Claude confidence; verbal confidence is not a calibrated probability. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver calibration-report.md, probability rows, reliability-bin counts, Python implementation, and tests. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Check p=[0.9,0.8,0.4,0.1], y=[1,0,1,0] by hand: Brier=0.255. Compare with constant p=0.5, Brier=0.25. Test empty input, NaN, endpoints, and invalid labels. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Can better threshold accuracy guarantee a better probability score?

<details>
<summary>Check your explanation after answering</summary>

No. Threshold accuracy discards confidence magnitude; Brier score uses it.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Irreducibly Human

[Reading map: metacognitive and supervisory work](../../docs/reading-map.md#irreducibly-human). Chapter 4's discussion of monitoring motivates comparing confidence with actual results.

**AI should** draft candidate code, calculate metrics, propose counterexamples, and help organize the evidence for this artifact.

**Human should** make the initial prediction, work through one calculation or case, choose the criterion that matters, inspect the evidence, and own the conclusion and authorized handoff. Record what you accepted, changed, rejected, or still do not understand in CONTRIBUTIONS.md. Do not invent a human review.

