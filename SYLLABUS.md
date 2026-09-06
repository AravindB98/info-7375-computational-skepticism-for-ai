# INFO 7375 — Computational Skepticism for AI

**Fall 2026 · NEU course adaptation**

## Course description

Students learn to interrogate AI outputs by building the mechanisms used to check them. Probability, data provenance, robustness, explanation, bias, fairness, agent validation, communication, and accountability become inspectable Python artifacts. Claude Code supports implementation and critique; students practice the underlying reasoning and own the conclusions. The semester culminates in a reproducible contribution that another person can inspect and challenge.

## Pedagogy

**Predict → Build It → Use It → Ship It → Verify**

Predict an outcome before seeing it. Build a small Python mechanism. Use it in a concrete Claude-assisted workflow. Ship an inspectable candidate. Verify that candidate against evidence independent of its narration, then revise when needed. The [course template](NEU-COURSE-TEMPLATE.md) defines each stage. Reading and reflection support the stages; they do not replace the artifact.

## Outcomes

By completing the course, students should be able to:

- Turn a plausible claim into an explicit prediction, assumption, and falsification test.
- Implement and explain calibration, data-audit, robustness, and group-metric calculations.
- Distinguish explanation, statistical association, causal claims, and evidence of actual system state.
- Design testable delegation contracts and approvals tied to a specific action.
- Communicate a result with appropriate uncertainty and source traceability.
- Produce an honest effort log, identify human and AI contributions, and deliver a reproducible final version.

## Access and preparation

Claude Code access through NEU is assumed. Start with the [prerequisites](prerequisites/README.md), including the university portal and [AI Policy for Professor Bear's Courses | Using AI Responsibly in Class](https://youtu.be/8Ut0Cdl6vMw?si=9w3aEpt1ZyAR4Kiz). Independent readers need their own Claude Code-enabled account. Python code runs locally using the standard library; direct Claude API calls are optional extensions and may consume separate API credits. No paid media service is required.

## Reading and sequence

The [course index](README.md) maps fifteen lessons to explicit book files. The [reading map](docs/reading-map.md) selects among duplicate chapter versions and gives targeted companion readings in Prompt Engineering for Generative AI, Conducting AI, Irreducibly Human, and Branding and AI. The existing chapters are the narrative book; lessons are the practice edition. Historical incident and philosophical claims in manuscripts should be evaluated with the same skeptical method as model outputs.

Lessons 1–3 establish claims, probability, and data provenance. Lessons 4–7 test robustness, explanations, bias, and fairness. Lessons 8–9 inspect agent outcomes and handoffs. Lessons 10–12 address honest presentation, uncertainty, and accountability. Lessons 13–15 challenge conclusions, build an audited artifact, and verify the capstone.

## Assessment and grading

Lesson exercises and knowledge checks are **ungraded Assessments**. Ten graded [Assignments](assignments/fall-2026/README.md) occur on a ten-day cadence; Canvas supplies actual dates. Each is worth 100 points:

| Component | Points |
|---|---:|
| Implementation of the specified exercises | 60 |
| Frictional: honest effort and learning | 10 |
| Proper GitHub version posting | 10 |
| Relative Quartile | 20 |
| Total | 100 |

Wrong initial predictions do not lose points by themselves. Failed attempts can earn full Frictional credit. No student must invent a defect or a struggle. Videos, including Brutalist explainers, are optional communication formats within Relative Quartile; no video has separate points. Course films belong in youtube/.

Submit a matching revision to Canvas and the designated GitHub location under fall-2026/first-name-last-initial/assignment-XX/. Include the final commit hash. Public deployment is not required. The [rubrics](prerequisites/README.md) separate effort, delivery, implementation, and comparative quality.

## AI and academic practice

Credit sources and assistance. Preserve original predictions, label synthetic and simulated evidence, and explain what you personally attempted, checked, revised, and decided. Claude may help compute, write, and critique; it may not invent your history, approval, observations, or learning. Students must be able to explain the work they submit. The instructor's linked AI policy applies to every Assignment.

## Official section information

Canvas supplies instructor contact, meeting times, office hours, first due date, final grade aggregation, letter-grade scale, attendance, late work, resubmission rules, quartile tie handling, and the official university policy text for the section. Those details have not been supplied for this book. This adaptation does not invent or replace university boilerplate. See [instructor decisions](docs/instructor-decisions.md).

