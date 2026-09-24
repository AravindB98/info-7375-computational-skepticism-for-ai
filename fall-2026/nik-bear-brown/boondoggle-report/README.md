# The Boondoggle Report — greenhouse-watch

**Application:** greenhouse-watch, the Reallocation Engine's job-board watcher, specified with Gru as a *corrective* design document.

## Executive summary

**What this is.** Professor Bear's worked example of the Week 2 assignment ([`BRIEF.md`](BRIEF.md)): a Software Design Document written with Gru, then a Boondoggle Score that splits the build between Claude and the human, then a reflection on that split. It is **in progress**. So far it covers the problem formulation gate (`/v0`, confirmed) and most of problem intake (`/v1`).

**Why read it.** It shows the gates doing their job on a real tool rather than a made-up one. Gru didn't accept the first sentence, and its questions turned up design problems in a skill that already exists and has already run on real job boards.

**What it has found so far.**
- **The first formulation was three sentences in one.** Gru split it into the thing, the trigger, and the output, and flagged that "fits their résumé" was carrying the whole design undefined ([turn 01](gru-session/01-v0-first-formulation.md)).
- **The watcher would give a second, competing verdict.** The engine already has a role scorer that says Apply, Consider, or Skip. Gru made the sentence say what the watcher's output *is* next to it: a notice, not a verdict ([turn 03](gru-session/03-v0-existing-components.md)).
- **Two phrases contradicted earlier answers.** The name says Greenhouse but the skill reads three platforms, and "the front of the engine" contradicted "runs beside the scorer." Both were fixed in the confirmed sentence ([turns 04–05](gru-session/04-v0-one-sentence.md)).
- **The real failures are in matching, not detection.** Evidence from real runs: a Writer board where 51 of 51 postings came back relevant because of company boilerplate, and a London role flagged for a student in Boston. Gru separated these into two different fixes ([turn 07](gru-session/07-v1-user-and-failures.md)).
- **It became a corrective SDD.** Because the skill already exists, the document specifies how to fix it, with today's version as the baseline ([turn 08](gru-session/08-v1-corrective-sdd.md)).
- **Five open questions are logged**, including whether the job boards even separate job text from company text ([turn 09](gru-session/09-v1-what-it-gives-priya.md)).

**What it has not done yet.** `/v1` question 6 onward, `/v2`–`/v4`, `/s1`, `/claude`, the paragraph after the Problem Summary, and the four-part reflection.

---

## Where each deliverable stands

| Deliverable | Status | Where |
|---|---|---|
| `/v0` problem formulation | ✅ confirmed after two rounds of pushback | turns 01–05 |
| `/v1` problem intake | 🟡 questions 2–5 answered; 6 onward next | turns 05–09 |
| Paragraph after the Problem Summary (own voice) | ⬜ after `/v1` closes | — |
| `/v2` principles, `/v3` flows, `/v4` needs | ⬜ | — |
| `/s1` components | ⬜ | — |
| `/claude` Boondoggle Score | ⬜ | — |
| Reflection, prompts A–D | ⬜ | — |

## The confirmed `/v0` sentence

> greenhouse-watch is a Claude Code skill that a student runs as an entry point to the Reallocation Engine, beside the role scorer and feeding nothing into it, reading one company's public job board on Greenhouse, Ashby, or SmartRecruiters plus the student's résumé JSON and remembering which job ids it saw last run, that produces a notice, not a verdict: a Markdown report and a JSON log listing only the postings new since the last run that match the résumé under a written string-match scheme, each with the résumé field and posting field behind every match.

## Open questions Gru has logged so far

Copied from Gru's own log (turns 05–09); Gru's wording is authoritative.

| # | Question | Blocks |
|---|---|---|
| OQ-1 | Which posting fields the match scheme may use (it must exclude repeated company text), and the match threshold | `/d1` |
| OQ-2 | The name "greenhouse-watch" misleads, since the skill also reads Ashby and SmartRecruiters | release |
| OQ-3 | Should `location_mode` default to soft or hard? Depends on how reliable each platform's location field is | `/v2` |
| OQ-4 | The `priya-nair` persona file in the engine repo has a calendar that doesn't match a running visa clock | — |
| OQ-5 | Do the three platforms keep company text in a separate field, or inside the job description? | OQ-1 |

## How the Gru session was run

See [`gru-session/README.md`](gru-session/README.md): the prompt, the method, what differs from running Gru in a Claude Project, and who typed Professor Bear's side of the conversation.
