# Lesson 1 — A claim you can try to break

**Predict → Build It → Use It → Ship It → Verify**

Reading: [the skeptics toolkit](../../chapters/01-the-skeptics-toolkit.md) — What I mean by skepticism. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: basic Python lists, dictionaries, functions, and file reading; complete the NEU setup if enrolled. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Which of three plausible claims will survive a check against its source? Write a confidence estimate and a possible falsifier for each. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Implement a Python claim ledger: claim ID, exact claim, source path, observation, check method, status, and remaining uncertainty. Reject missing IDs, duplicate IDs, and unknown statuses. A status of supported must point to evidence; it must not be inferred from fluency. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/01-skeptics-toolkit/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Give Claude Code a small local source packet and ask for three claims with source locations. Choose and check the claims yourself, then ask Claude to propose a counterexample. Record which source actually supports each claim. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver claim-ledger.json, your original predictions, a source packet, tests, and a short verdict. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Use one supported, one contradicted, and one unresolved synthetic example. Manually trace each status. A missing source must produce unresolved, never supported. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. What distinguishes a checkable falsifier from a general expression of doubt?

<details>
<summary>Check your explanation after answering</summary>

A falsifier specifies an observation that would count against a particular claim.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Conducting AI

[Reading map: solve–verify asymmetry](../../docs/reading-map.md#conducting-ai). The companion's Chapter 2 distinguishes producing an answer from grounding it in the relevant world, and considers tool-assisted verification as a counter-case. Name the external source, state, or calculation that grounds your result. Identify shared assumptions that could make your second check repeat the first error.

