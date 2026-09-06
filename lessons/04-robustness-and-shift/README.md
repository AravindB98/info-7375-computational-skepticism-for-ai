# Lesson 4 — Break the shortcut you just built

**Predict → Build It → Use It → Ship It → Verify**

Reading: [robustness what understanding means when a pixel can break the model](../../chapters/04-robustness-what-understanding-means-when-a-pixel-can-break-the-model.md) — Prompt sensitivity — the LLM-specific version of this problem. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–3, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Which input changes should preserve the result, and which should change it? Name the distinction before designing probes. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement a deterministic Python probe runner recording baseline input, transformed input, expected relation, observed output, and pass/fail. Include whitespace or ordering invariance, a relevant semantic change, and a shifted slice. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/04-robustness-and-shift/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to critique your probe expectations and suggest a shortcut your implementation may exploit. Run at least three frozen probes on your own small classifier or prompt workflow. Keep live Claude observations separate from an offline surrogate. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver robustness-profile.csv, the baseline mechanism, probes, failures, and a residual-risk note. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Use a known fragile baseline to establish that at least one probe can fail, then a targeted repair. Do not claim every perturbation preserves meaning. A passing finite suite is evidence only about those probes. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. What does zero observed failures establish?

<details>
<summary>Check your explanation after answering</summary>

Only performance on the tested inputs and expectations, within the recorded conditions.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.


