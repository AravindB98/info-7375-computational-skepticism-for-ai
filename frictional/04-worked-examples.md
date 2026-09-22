# Worked Examples: A Thin Log and a Strong One

**What this page is.** Two Frictional logs for the same Assignment, scored row by row on the [official rubric](../prerequisites/frictional.md). One earns 2/10. One earns 10/10. Read this page before your first submission — it is the fastest way to see what *specific and sufficient* means.

**Both students shipped working code.** On the 60 implementation points they would score within a few points of each other. The Frictional gap is 8 points, which is most of a letter grade on the Assignment.

> **These are constructed teaching examples, not real student work.** They were written to illustrate the rubric. No student wrote either one.

---

## The Assignment both students did

[Assignment 1](../assignments/fall-2026/assignment-01.md) — a Python claim ledger with status validation, plus mean squared probability error with reliability bins and an explicit convention for p=1. Hand check: `p=[0.9,0.8,0.4,0.1], y=[1,0,1,0]` gives Brier 0.255; constant `p=0.5` gives 0.25.

---

## Log A — 2/10

> **FRICTIONAL.md**
>
> **10/12** — Started the assignment. Read the lesson and set up the repo. Implemented the claim ledger. It was a bit confusing at first but I figured it out.
>
> **10/14** — Did the Brier score part. Used Claude to help with some of the code. Got the tests passing. Calibration was tricky but it works now. Finished the README and pushed everything. Overall I learned a lot about calibration.

### Scoring

| Row | Score | Why |
|---|---:|---|
| Attempts | 1 | Names activities ("implemented the ledger") but no expectation anywhere. Nothing was predicted, so nothing can have been violated. |
| Friction and response | 0 | "A bit confusing," "tricky." These name categories of experience, not experiences. No object, no check, no response. |
| Human and AI contributions | 1 | Claude is disclosed — that is honest and it is worth something. But "help with some of the code" does not say what was accepted, changed, or rejected. |
| Learning and uncertainty | 0 | "Learned a lot" is content-free and nothing is named as unresolved. |
| Traceable process | 0 | Two dates, no commits, no test names, no outputs. Nothing a reviewer can open. |
| **Total** | **2** | |

**The point of Log A:** this student may have done every bit of the work. That is the problem. They submitted an artifact indistinguishable from a generated one and a log indistinguishable from a generated one. The 2 is not an accusation — it is the honest statement that the evidence does not support more. Every sentence in Log A could have been written by someone who never opened the repository.

---

## Log B — 10/10

> **FRICTIONAL.md**
>
> **10/12** — *What I tried and expected:* Built the ledger schema first. Expected the duplicate-ID rejection to be the fiddly part.
> *What happened / what I checked:* It wasn't. The hard part was `status: supported`. My first version let the caller set it directly, which means a fluent-sounding claim can be marked supported with no source. That is exactly the failure the lesson is about and I had written it into my own schema.
> *What I did next:* Made `supported` unreachable except through a path that requires a non-empty `source_path` plus an `observation`. Missing source now yields `unresolved`, never `supported`.
> *Contributions:* Mine. Claude not used yet.
> *Understand / do not understand:* Understand that the validation has to make the bad state unrepresentable rather than merely discouraged. Do not yet know whether `unresolved` and `contradicted` need to be distinguishable when the source is missing entirely.
> *Evidence:* `test_missing_source_yields_unresolved`; commit `feat: make supported unreachable without source evidence`. Next: the Brier work.
>
> **10/14** — *Tried and expected:* Implemented MSPE, then ran the hand check from PREDICTIONS.md. Predicted the informative vector (0.9/0.8/0.4/0.1) would beat constant 0.5, because it is obviously carrying more information.
> *What happened:* It loses. 0.255 against 0.250. I re-ran it three times assuming an arithmetic error, then did the four rows by hand on paper. The hand calculation agrees. The prediction was wrong.
> *What I did next:* Sat with it. The 0.8-on-a-0 row contributes 0.64 by itself, which is more than the entire constant predictor's average. One confident miss outweighs three good calls. I had assumed "more informative" implied "better scored" and those are different properties.
> *Contributions:* Mine, including the hand check.
> *Understand / do not understand:* Understand that a proper scoring rule punishes confident errors superlinearly, and that a baseline beating you is information about your confidence, not only about your accuracy. Do not understand how I would have caught this if the assignment had not handed me the baseline — I do not know how to pick a baseline in general.
> *Evidence:* `test_brier_matches_hand_calculation` (0.255); photo of the paper check in `evidence/hand-check-1014.jpg`; commit `test: pin hand-verified Brier against constant baseline`. Next: reliability bins.
>
> **10/15** — *Tried and expected:* Reliability bins, ten of them. Expected counts to sum to the row count.
> *What happened:* They sum to 39 of 40. One row is disappearing. p=1.0 falls outside every bin because all ten are half-open under my `<` comparison.
> *What I did next:* Asked Claude why a bin count could come up short. It gave three candidate causes; the half-open-interval one matched. It then proposed special-casing p=1.0 into the last bin. **I rejected that fix** — it puts the convention in two places, and the next person to read the code would not find it. Instead I made the final bin closed on the right and stated the convention in the README as a claim about the data rather than an implementation detail. Claude located the cause; the design decision is mine.
> *Contributions:* Claude — diagnosis accepted, proposed fix rejected, replacement written by me. Transcript in `evidence/claude-bins-1015.md`.
> *Understand / do not understand:* Understand that a binning convention is an assertion that has to be declared. Still do not understand how to choose ten bins over five — I used ten because the lesson did, and I cannot defend it. Noted as a limit in VERIFICATION.md.
> *Evidence:* `test_reliability_bin_endpoint`; commit `fix: close final reliability bin so p=1.0 is counted`.
>
> **10/16 (retrospective, written 10-17)** — *Tried and expected:* Final pass; expected only README edits.
> *What happened:* Re-reading the ledger with the Brier result in mind, I noticed my `remaining_uncertainty` field is free text nobody validates, which is the same weakness as the original `supported` problem in a quieter form. Out of scope to fix now.
> *What I did next:* Left it, and named it in VERIFICATION.md as a known limit rather than pretending it isn't there.
> *Contributions:* Mine.
> *Understand / do not understand:* Understand that the schema encodes an epistemics, and unvalidated fields are where unsupported claims re-enter. Do not know whether validating free text is possible without making the field useless.
> *Evidence:* VERIFICATION.md limits section; commit `docs: record unvalidated uncertainty field as known limit`.

### Scoring

| Row | Score | Why |
|---|---:|---|
| Attempts | 2 | Every entry states what was tried and what was expected. The 10/14 prediction is specific enough to be *wrong*, which is what makes it worth 2. |
| Friction and response | 2 | Four specific frictions, each anchored to an object — the `supported` path, 0.255 vs 0.250, 39 of 40, the free-text field — each with what was done next, including one thing left undone and declared. |
| Human and AI contributions | 2 | Claude's contribution is bounded precisely: diagnosis accepted, fix rejected, replacement written by the student, transcript preserved. The three entries with no AI use say so. |
| Learning and uncertainty | 2 | Something changed in every entry, and every entry names something still open. The 10/14 "I don't know how to pick a baseline in general" is the strongest line in the log. |
| Traceable process | 2 | Every entry cites a test, a commit subject, or a file. The retrospective entry is marked. |
| **Total** | **10** | |

---

## What actually separates them

Log B is not longer because the student worked harder or wrote better. It took roughly twelve minutes across four sessions. It is longer because it is **anchored**: every claim points at a specific object in the actual work.

Three moves do nearly all of the work, and you can copy all three:

1. **Write the expectation before the run.** You cannot record a violated prediction if you never recorded a prediction. This is the same discipline PREDICTIONS.md already asks of you.
2. **Name the object, not the category.** Not "the calibration part" — `0.255 against 0.250`, `39 of 40`, `test_reliability_bin_endpoint`.
3. **Say what you did with the help.** Accepted, changed, or rejected. Log B's highest-value entry is the one where Claude was *wrong for a reason the student could articulate*.

Before you submit, take any sentence in your log and ask whether a classmate who never opened your repository could have written it. If they could, you have written about the Assignment. Write about what happened instead.
