# Lesson 13 — Try to defeat your own conclusion

**Predict → Build It → Use It → Ship It → Verify**

Reading: [the limits of ai what the tools cannot do](../../chapters/13-the-limits-of-ai-what-the-tools-cannot-do.md) — What would change my mind. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–12, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Will your strongest result survive a new held-out case, a different assumption, and a second implementation? Register separate expectations. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Build a Python replication runner that compares an initial implementation with a separately derived check over frozen cases. Track agreement, disagreement, unsupported scope, and cases where both methods may share an assumption. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/13-limits-and-replication/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to formulate the strongest counterargument to your report. Test the measurable part. Separate an observed failure, a theoretical assumption, and a philosophical claim of impossibility. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver replication-report.md, independent check, frozen cases, disagreement log, and revised scope statement. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Include a planted shared-error case to show why agreement is insufficient. Repeat an earlier calibration task and compare your predictions with outcomes. Record actual findings even when the original claim survives. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Does agreement between two assistants demonstrate independent verification?

<details>
<summary>Check your explanation after answering</summary>

No. Shared sources, prompts, or assumptions can make their errors dependent.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Conducting AI

[Reading map: solve–verify asymmetry](../../docs/reading-map.md#conducting-ai). The companion's Chapter 2 distinguishes producing an answer from grounding it in the relevant world, and considers tool-assisted verification as a counter-case. Name the external source, state, or calculation that grounds your result. Identify shared assumptions that could make your second check repeat the first error.

