# Lesson 9 — A handoff needs a condition someone can check

**Predict → Build It → Use It → Ship It → Verify**

Reading: [delegation trust and the supervisory role](../../chapters/09-delegation-trust-and-the-supervisory-role.md) — The handoff condition: the contract, not the partition. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–8, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Which step in a three-step AI workflow will be hardest for another person to approve? Identify the ambiguous word. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Build a Python handoff validator for owner, input, output, acceptance condition, evidence reference, and escalation destination. Separate schema completeness from a substantive judgment that evidence meets a condition. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/09-delegation-and-handoffs/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Have Claude draft a delegation map for your agent or data pipeline. Replace words such as reasonable and reviewed with observable criteria. Test the map against one passing case and one unresolved case. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver delegation-map.json, validator, acceptance examples, escalation route, and a human decision record. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Reject missing ownership and evidence. Demonstrate a schema-valid but substantively unacceptable packet. Only record a real person's approval when it occurred; label classroom role-play. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. What does schema validity establish about approval?

<details>
<summary>Check your explanation after answering</summary>

It establishes required structure, not evidence quality, authority, or actual consent.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Conducting AI

[Reading map: solve–verify asymmetry](../../docs/reading-map.md#conducting-ai). The companion's Chapter 2 distinguishes producing an answer from grounding it in the relevant world, and considers tool-assisted verification as a counter-case. Name the external source, state, or calculation that grounds your result. Identify shared assumptions that could make your second check repeat the first error.

