# Lesson 5 — A convincing explanation can explain the wrong thing

**Predict → Build It → Use It → Ship It → Verify**

Reading: [model explainability distinguishing explanation from the appearance of explanation](../../chapters/05-model-explainability-distinguishing-explanation-from-the-appearance-of-explanation.md) — Three words that don't mean the same thing. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–4, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Will the feature named in a fluent explanation be necessary for the output? Predict a concrete removal test. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Build an interpretable Python scoring rule with two or three features and a counterfactual enumerator over a small discrete input space. Report original score, changed feature, new score, decision change, and feasibility constraints. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/05-explanations-and-counterexamples/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude to explain the rule from examples, then compare its narrative with executed feature changes. Test a correlated proxy and a feature with no effect. Label model sensitivity separately from real-world causation. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver explanation-audit.md, scoring rule, counterfactual table, feasibility assumptions, and tests. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Compute at least two cases by hand. Test unchanged inputs, unreachable target decisions, and infeasible feature changes. A counterfactual of a program does not demonstrate an intervention on the world. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Does a feature attribution establish the cause of a real-world outcome?

<details>
<summary>Check your explanation after answering</summary>

No. It describes a model under specified assumptions; causal claims need additional evidence.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.


