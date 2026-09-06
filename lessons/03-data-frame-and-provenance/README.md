# Lesson 3 — The missing rows are part of the result

**Predict → Build It → Use It → Ship It → Verify**

Reading: [data validation reconstructing the epistemic frame behind a dataset](../../chapters/03-data-validation-reconstructing-the-epistemic-frame-behind-a-dataset.md) — Reconstructing the epistemic frame — a working procedure. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–2, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

From two small CSV schemas, predict the join row count and who might disappear. Lock your estimate before inspecting the joined output. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Build a Python CSV audit that reports key uniqueness, unmatched keys on both sides, row counts before and after the join, and missing values. Define whether duplicate keys are an error or a many-to-many join. Preserve raw input. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/03-data-frame-and-provenance/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Use Claude Code to propose a join and a datasheet. Reconstruct sampling, time window, label proxies, missingness, transformations, and boundaries yourself. Trace one record back to its source; document opacity when the source is unavailable. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver join-audit.json, two source CSVs, datasheet.md, a row trace, and tests. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Use left IDs [a,b,c], right IDs [a,b,d]: an inner join returns two keys, while c and d disappear from opposite sides. Add duplicate-key and absent-column cases. Check the output against the expected population, not only its schema. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Why can a file with no missing cells still misrepresent its population?

<details>
<summary>Check your explanation after answering</summary>

Rows may have been excluded before the file existed; cell-level checks cannot recover them.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Prompt Engineering for Generative AI

[Reading map: prompt contracts](../../docs/reading-map.md#prompt-engineering-for-generative-ai). The companion course's Lesson 2 makes input, output, and validation explicit. Turn the instruction you gave Claude into such a contract, and compare a validly formatted response with one that is actually supported by your source data.

