# Lesson 10 — One dataset, two stories

**Predict → Build It → Use It → Ship It → Verify**

Reading: [visualization under validation honest misleading and the choices between](../../chapters/10-visualization-under-validation-honest-misleading-and-the-choices-between.md) — The deceptive visualization catalog. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–9, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

How will changing the axis baseline alter perceived improvement without changing a single value? Sketch both views first. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Use Python to produce two SVG bar charts from the same small CSV: one starting at zero and one clearly labeled truncated-axis demonstration. Print values, units, sample size, and transformation choices alongside them. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/10-visualization-under-validation/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to critique the message each chart conveys. Make an honest final chart for a named reader, including relevant uncertainty or a clear statement that the dataset cannot estimate it. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver chart-comparison.md, both labeled teaching SVGs, source CSV, generation script, and final chart. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Verify bar geometry against source numbers and labels. Test equal values, zero range, and negative inputs according to your documented chart contract. Ship the misleading demonstration only with its explanatory comparison. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Can accurate numbers still produce a misleading chart?

<details>
<summary>Check your explanation after answering</summary>

Yes. Encoding, aggregation, and selection can distort the impression made by accurate numbers.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Branding and AI

[Reading map: Portfolio as Product](../../docs/reading-map.md#branding-and-ai). Chapter 18 distinguishes GitHub's inspectable technical evidence from the audience-facing case study. Write a short explanation for a reader who has two minutes, and point it to the exact evidence a technical reviewer needs. Check that both tell the same bounded story. A video is optional.

