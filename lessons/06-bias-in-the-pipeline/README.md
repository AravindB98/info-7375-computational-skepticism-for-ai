# Lesson 6 — Find the decision that produced the disparity

**Predict → Build It → Use It → Ship It → Verify**

Reading: [bias where it enters and who is responsible](../../chapters/06-bias-where-it-enters-and-who-is-responsible.md) — chapter reading. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–5, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

At which pipeline step will the biggest group difference appear: sampling, labels, filtering, or thresholding? State an expected direction. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement a Python pipeline audit that records group counts and positive rates before and after each transformation. Use synthetic groups A and B. Make a deliberate biased filtering rule, then measure the effect of removing it. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/06-bias-in-the-pipeline/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to generate alternative explanations for your observed gap. Draw the path from collection to action and identify which hypothesis your data can distinguish. Treat synthetic groups as teaching constructs, not real demographic findings. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver pipeline-audit.csv, transformation code, an assumptions diagram, and an intervention comparison. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Preserve denominators at every step, test an empty group, and recompute one group rate by hand. Compare the proposed repair with a baseline on the same frozen rows. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Why is finding a group gap insufficient to identify its cause?

<details>
<summary>Check your explanation after answering</summary>

Several upstream processes can produce the same observed gap.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.


