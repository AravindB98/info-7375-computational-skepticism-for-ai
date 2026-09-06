# Lesson 14 — Build something worth auditing

**Predict → Build It → Use It → Ship It → Verify**

Reading: [the skeptics toolkit](../../chapters/01-the-skeptics-toolkit.md) — Skepticism as a team practice. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–13, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Which two skeptical instruments are most likely to expose a weakness in your proposed build? Predict a measurable result for each. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Build a bounded Python artifact of your choice: dataset pipeline, classifier, prompt workflow, chart generator, or simulated agent. Implement two instruments from lessons 2–12 and define their input/output contracts before using them. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/14-build-and-break-studio/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Use Claude Code to help implement, debug, and challenge the build. Maintain a record of accepted, changed, and rejected suggestions. Request a peer critique when available; honestly record if no peer participated. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver build-and-break-packet/ with runnable artifact, two audits, source credits, evidence, and a scope statement. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Run the predeclared probes. Report a discovered defect or, if none was found, the tested boundary and residual uncertainty. Never invent a failure to satisfy a confession requirement. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. What makes a negative finding useful?

<details>
<summary>Check your explanation after answering</summary>

A clear scope, a discriminating check, and honest limits on what the absence of a failure means.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Branding and AI

[Reading map: Portfolio as Product](../../docs/reading-map.md#branding-and-ai). Chapter 18 distinguishes GitHub's inspectable technical evidence from the audience-facing case study. Write a short explanation for a reader who has two minutes, and point it to the exact evidence a technical reviewer needs. Check that both tell the same bounded story. A video is optional.

