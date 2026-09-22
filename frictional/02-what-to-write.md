# What to Write in FRICTIONAL.md

**What this page is.** The seven fields of [templates/FRICTIONAL.md](../templates/FRICTIONAL.md), what each one is actually asking for, and which rubric row it feeds.

**The short version.** Short dated entries, written while you work. One entry per work session. Fragments are fine; the log is not prose. Three or four entries for a ten-day Assignment is normal.

**The one thing that decides your score.** Specificity. Every row of the rubric awards 2 for *specific and sufficient*, 1 for *vague or incomplete*, 0 for *absent*. Nearly every point lost in this component is lost to vagueness, not to dishonesty or to bad results.

---

## The field-to-rubric map

The template is not arbitrary. Each field feeds a rubric row.

| Template field | Rubric row | Points |
|---|---|---:|
| What I tried and expected | Attempts | 2 |
| What happened / what I found difficult or checked · What I did next | Friction and response | 2 |
| What Claude or another person contributed | Human and AI contributions | 2 |
| What I understand now / still do not understand | Learning and uncertainty | 2 |
| Date (marked if retrospective) · Evidence, commit, and next step | Traceable process | 2 |

Fill all seven fields and you have covered all five rows. Skip a field and you have volunteered a zero.

---

## Field by field

### Date — mark retrospective entries
The date you did the work. If you are writing the entry later than the session it describes, say so: `2026-10-03 (retrospective, written 10-05)`. Marking it costs nothing and an unmarked retrospective that reads as contemporaneous is a fabrication problem, not a style problem.

### What I tried and expected → *Attempts*
The attempt, and the prediction that went with it. The prediction is the part people skip and it is half the row.

> Weak: *Worked on the Brier implementation.*
>
> Strong: *Wrote the reliability binning. Expected the p=1 edge case to land in the top bin; wanted to confirm before writing the convention into the README.*

An attempt that failed earns the same 2 points as one that worked. This row scores whether you can say what you were doing and what you thought would happen.

### What happened / what I found difficult or checked → *Friction and response* (first half)
The place the work resisted. **Name the object.** "It was confusing" names a category of experience, not an experience.

> Weak: *The calibration part was confusing at first.*
>
> Strong: *p=1 lands in the top bin under my `<` comparison but the last bin is half-open, so one row silently vanished from the counts. Totals summed to 39, not 40.*

A check you ran counts here too, even when it found nothing — "checked whether the ledger rejects duplicate IDs; it does" is a specific, sufficient entry.

### What I did next → *Friction and response* (second half)
What you did about it, including approaches you abandoned and why. Dead ends are worth more than the fix, because a dead end you can describe is proof you were somewhere.

> *First tried special-casing p=1, which worked but meant the convention lived in two places. Backed that out and made the last bin closed instead, documented in the README. Added a test at exactly 1.0.*

### What Claude or another person contributed → *Human and AI contributions*
Who or what helped, what it produced, and what you **accepted, changed, or rejected**. That last clause is the graded part. Naming the tool without naming the disposition is a 1, not a 2.

> Weak: *Used Claude for the binning code.*
>
> Strong: *Asked Claude why a bin count could be short. It suggested three causes; the half-open interval one matched. Rejected its proposed fix (special-case at 1.0) because it duplicates the convention. Wrote the closed-bin version myself. Claude found the cause; the design decision is mine.*

Human help is logged identically — study group, TA, a classmate, Stack Overflow. This is a contributions record, the same thing an acknowledgments section is. It is not a confession.

### What I understand now / still do not understand → *Learning and uncertainty*
What changed, and what is still open. **"Nothing is unresolved" is almost never true** and reads as the least credible available answer. Name something.

> *Now understand that a binning convention is a claim about the data and has to be stated, not assumed. Still do not understand how to choose bin counts — I used ten because the lesson did, and I cannot defend ten over five.*

Naming a limit in your own work scores well here. It is the same move the course asks for in VERIFICATION.md.

### Evidence, commit, and next step → *Traceable process*
The link between this entry and something inspectable: a commit hash or subject, a test name, an output file, a prompt transcript, a draft.

> *Evidence: `test_reliability_bin_endpoint`; commit `fix: close final reliability bin so p=1.0 is counted`. Next: hand-check the four-row example from the prediction.*

Commit volume is not graded — [GitHub posting](../prerequisites/github-submission.md) says so explicitly — but a log whose entries point at nothing inspectable cannot earn this row.

---

## How much to write

An entry is three to six lines. A ten-day Assignment usually produces three to five entries. If an entry is running past a paragraph per field you are writing an essay about your process instead of logging it.

The floor that works: **one entry per work session, dated, with all seven fields answered, even when the answer is short.** "Nothing resisted today; ran the tests, all passed, checked the endpoint case by hand" is a legitimate entry and will not cost you points.

## Before you submit

- [ ] Every entry is dated, and retrospective entries are marked
- [ ] At least one entry names a specific object — a value, a test, a line, a filename — not a category
- [ ] At least one thing that did not work is written down, with why you moved off it
- [ ] Every AI and human contribution says what you accepted, changed, or rejected
- [ ] Something is named as still unresolved
- [ ] Entries point at commits, tests, or outputs a reviewer can open
- [ ] `FRICTIONAL.md` is in `fall-2026/first-name-last-initial/assignment-XX/` and the Canvas version matches
