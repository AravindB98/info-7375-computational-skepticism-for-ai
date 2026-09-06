# Lesson 8 — The agent said done. Check the state.

**Predict → Build It → Use It → Ship It → Verify**

Reading: [validating agentic ai when autonomous systems misbehave](../../chapters/08-validating-agentic-ai-when-autonomous-systems-misbehave.md) — From prediction to action. See [reading notes](../../docs/reading-map.md) for editorial cautions. Tools: Python standard library and Claude Code. Prerequisites: Lessons 1–7, especially their retained evidence and predictions. Suggested session: one class meeting plus independent practice; Canvas controls pacing.

## Predict

Will an agent transcript saying success correspond to the intended final state in every fixture? Identify a failure predicate first. Save the prediction in PREDICTIONS.md before the run, including a confidence estimate and what would change your mind. Do not overwrite it with the observed result.

## Build It

Build a Python state-machine simulator with allowed actions, bounded steps, action-result logs, and a separate final-state checker. Include a success message whose underlying state remains unchanged. Make a first attempt before asking Claude for a complete solution. Work in learning-artifacts/08-agent-outcomes-and-traces/. Write main.py and test_main.py; a deliberately small mechanism is enough when its behavior and limits are clear.

## Use It

Ask Claude Code to propose action sequences against your local simulator. Run the sequences with no external accounts or consequential tools. Record transcript, tool result, and final state as separate evidence types. Record the model identifier as displayed, date, relevant prompt excerpt, commands, and actual outputs. Label an offline fixture explicitly. Do not report a simulated result as a live Claude call. No direct API credits are required.

## Ship It

Deliver agent-trace.json, simulator, outcome checks, success and failure fixtures, and diagnosis. Add a README with the purpose, inputs, exact run/test commands, and known limitations. Include PREDICTIONS.md, CONTRIBUTIONS.md, and FRICTIONAL.md using the [shared templates](../../templates/README.md). Package a local candidate ready for inspection. The [graded Assignment map](../../assignments/fall-2026/README.md) explains which candidate belongs to which submission.

## Verify

Test genuine completion, falsely narrated completion, unauthorized action, and exhausted budget. Let the outcome checker reject a plausible success transcript. This is a simulator, not a live incident reproduction. Run the checks on the packaged version, not only the development copy. Record actual commands and observed outcomes in VERIFICATION.md, compare them with your prediction, and explain any change in understanding. Fix a failed candidate, ship the revision, and verify again. Preserve unresolved limitations.

### Assessments — ungraded

1. Complete the five-stage artifact and its boundary checks.
2. Explain the mechanism without relying on Claude's prose.
3. Why should an outcome checker inspect state independently of narration?

<details>
<summary>Check your explanation after answering</summary>

A success statement records what was said; the state records what the action actually changed.

</details>

These are practice Assessments, not separately graded weekly work. See the ten-day Assignment brief for the 100-point submission.

## Anthropics

[Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents), checked 2026-09-06. Compare its distinction between transcripts and outcomes with your simulator's trace and final-state assertion. Identify the outcome your grader can inspect directly. This small classroom simulator is our adaptation, not Anthropic's agent implementation; no direct API call is required.

