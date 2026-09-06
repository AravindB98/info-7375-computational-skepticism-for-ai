# Lesson 12 — An approval belongs to a particular action

**Predict → Build It → Use It → Ship It → Verify**

Reading: [accountability who is responsible when the system fails](../../chapters/12-accountability-who-is-responsible-when-the-system-fails.md) — The gate: the attestation you sign. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–11, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

If a target changes after approval, should the approval still permit execution? Specify the rule before implementing it. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement a Python proposal fingerprint over canonical JSON and bind an approval record to that fingerprint. Record owner, scope, evidence, decision, and expiration. Use a fixed injected clock in tests. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/12-accountability-and-gates/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to identify gaps in the approval packet for your existing workflow. Have a person make the classroom review decision or label a simulated decision. Do not connect this teaching gate to real consequential systems. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver approval-packet.json, fingerprint implementation, expiry tests, changed-target test, and responsibility map. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Test changed target, changed effect, absent approval, expired approval, and matching approval. Explain that a hash alone does not authenticate a signer or secure a production system. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. What happens when an approved proposal changes?

<details>
<summary>Check your explanation after answering</summary>

The prior approval no longer matches; review the new proposal.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Conducting AI

[Reading map: solve–verify asymmetry](../../docs/reading-map.md#conducting-ai). The companion's Chapter 2 distinguishes producing an answer from grounding it in the relevant world, and considers tool-assisted verification as a counter-case. Name the external source, state, or calculation that grounds your result. Identify shared assumptions that could make your second check repeat the first error.

