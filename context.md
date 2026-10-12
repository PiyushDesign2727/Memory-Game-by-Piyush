# AI PM Portfolio — Project Context

## Purpose

This repository is being prepared as the foundation for **[YOUR NAME]'s AI
Product Manager portfolio**. The portfolio should make product judgment
visible: how the author identifies real user problems, makes trade-offs,
coordinates delivery, and measures outcomes—including the additional
evaluation, reliability, safety, and privacy considerations relevant to AI
products.

This is a portfolio starter, not evidence that the owner has a particular job
title, shipped an AI product, achieved a metric, or led a project. Those facts
must come from the owner and be verified before publication.

## Current repository state

The repository currently contains two self-contained browser games and their
requirements examples:

- `memory-game.html`: Memory matching game with 4×4 and 6×6 boards, a
  light/dark theme preference, keyboard and mouse interaction, a timer, move
  rating, and saved high scores.
- `snake.html`: Snake game with keyboard and on-screen direction controls,
  pause/resume, score, a saved best score, and system color-scheme styling.
- `PRD_dark_theme.md`: Requirements and verification checklist for the Memory
  Game theme feature.
- `PRD_snake.md`: Requirements and verification checklist for Snake.
- `README.md`: Portfolio purpose, setup, content guidance, and instructions for
  running the current game demos.

The games demonstrate self-contained product prototypes and supporting
requirements. They are **not AI products**. A portfolio case study may include
them only after the owner supplies their actual role, decisions, process,
validation, and outcomes. Do not infer personal ownership, user research,
business impact, or AI expertise from the code alone.

## Intended audience

- Recruiters and hiring managers evaluating product judgment and communication.
- Product, design, engineering, data, and research peers.
- Potential collaborators who need a concise view of the author's interests
  and approach.

Assume readers scan quickly. Lead with a clear value proposition and link to a
small number of detailed, evidence-rich case studies.

## Portfolio objectives

The finished portfolio should:

1. Explain the author's product focus and the kinds of problems they solve.
2. Show end-to-end thinking, from discovery through delivery and measurement.
3. Make the author's individual contribution explicit within team work.
4. Demonstrate prioritization, trade-offs, communication, and learning.
5. Show sound AI product judgment when the work genuinely involves AI.
6. Be accessible, responsive, easy to navigate, and straightforward to
   maintain.

## Required information from the owner

Use conspicuous placeholders until the owner provides and confirms:

- Name, preferred role title, location if desired, and contact method.
- Professional summary and target roles or product domains.
- Work history, responsibilities, collaborators, and project dates.
- Case studies the owner is authorized to share.
- Their role and specific contributions for each case study.
- Validated goals, baselines, outcomes, time periods, and attribution caveats.
- Links to LinkedIn, resume, products, demos, or public artifacts.
- Any privacy, confidentiality, accessibility, or branding requirements.

Do not fill these fields from assumptions, repository metadata, commit identity,
or generated examples.

## Case-study standard

Each case study should answer:

1. **Context:** What product, customer group, team, timeframe, and project
   status are relevant?
2. **Problem:** What user or business problem mattered, and what evidence
   showed it was worth solving?
3. **Role:** What was the author's responsibility and what did they personally
   decide or deliver?
4. **Strategy:** What goal, product principles, options, prioritization method,
   constraints, and trade-offs guided the work?
5. **Execution:** How did product, design, engineering, data, research, legal,
   or operations collaborate? What was built, tested, and launched?
6. **Measurement:** What were the baseline, target, metric definitions,
   guardrails, measurement period, and observed results? What can and cannot be
   attributed to the work?
7. **Learning:** What did the team learn, what changed, and what would the
   author do next?

Label each project accurately as **shipped**, **in progress**, **prototype**,
**experiment**, or **proposal**. A prototype does not imply production usage.

## AI product case-study requirements

Only use this section when the project genuinely includes an AI system or
AI-enabled workflow. Explain:

- Why AI was appropriate relative to simpler deterministic alternatives.
- The user and business value expected from using AI.
- The user-facing behavior and where uncertainty or failure can occur.
- How quality was evaluated: representative examples, test methodology,
  baselines, acceptance thresholds, and known limitations.
- Relevant quality dimensions such as accuracy, groundedness, latency,
  reliability, fairness, abuse resistance, and cost.
- Human review, escalation, correction, fallback, and user-control mechanisms.
- Privacy, data handling, retention, access controls, safety, and applicable
  policy or legal review.
- Monitoring after launch, incident handling, and criteria for rollback or
  improvement.

Do not expose confidential prompts, model internals, customer data, private
evaluation sets, credentials, or sensitive vendor information. Generalize
examples only when that preserves truth and does not disclose protected data.

## Content integrity and responsible use

- Never invent achievements, users, research findings, quotes, metrics, or
  professional credentials.
- Distinguish direct measurement from estimates and qualitative evidence.
- State metric definitions, time periods, sample limitations, and attribution
  caveats where they affect interpretation.
- Credit collaborators and avoid presenting team results as solely individual
  work.
- Share only material the owner has permission to publish.
- Remove customer-identifying, employer-confidential, personal, and regulated
  data.
- AI-generated copy must be reviewed and fact-checked by the portfolio owner.
- Keep contact details and resume content intentionally public and current.

## Recommended information architecture

Planned sections for the portfolio site:

- **Home:** Name, role focus, concise positioning statement, selected work.
- **About:** Verified background, approach, and interests.
- **Case studies:** A curated set of detailed project stories.
- **AI product practice:** AI-specific work and evaluation, if supported by
  genuine experience.
- **Artifacts:** Shareable PRDs, prototypes, research, and operating
  frameworks.
- **Resume and contact:** Public resume and selected contact links.

Suggested starter structure (not all paths currently exist):

```text
index.html
about.html
case-studies/
  case-study-template.md
  project-one.md
assets/
  styles.css
  images/
resume/
  resume.pdf
memory-game.html
snake.html
PRD_dark_theme.md
PRD_snake.md
README.md
context.md
```

## Technical and design guidance

- Prefer a small static site first; add frameworks, APIs, databases, or analytics
  only for a demonstrated need.
- Preserve the existing game demos as independent HTML files.
- Keep content and presentation maintainable, reusable, and responsive.
- Use semantic HTML, descriptive link text, keyboard-accessible navigation,
  visible focus, appropriate color contrast, and reduced-motion support where
  animations are introduced.
- Optimize images and provide useful alternative text; avoid decorative
  animation that obstructs reading.
- Test at narrow and wide viewport sizes and in at least one keyboard-only
  workflow.
- Do not add third-party tracking without an explicit user need and appropriate
  disclosure.
- Never put secrets, access tokens, private datasets, or credentials in the
  repository.

## AI-assistant working instructions

When helping with this portfolio:

1. Read this file and the relevant project files before changing content or
   code.
2. Preserve the distinction between current repository contents and proposed
   portfolio structure.
3. Use placeholders for unknown biography, project, outcome, and contact facts.
4. Ask the owner for clarification when a missing fact changes the story,
   audience, or implementation direction.
5. Do not label the existing games as AI products unless the owner supplies
   truthful supporting context.
6. Keep edits focused, update related documentation, and test any functional
   web changes in a browser.
7. Summarize what changed and call out any placeholders the owner still needs to
   complete.

## Definition of ready to publish

The portfolio is ready to share only after:

- The owner has replaced and reviewed every placeholder.
- Every role, contribution, date, outcome, and metric is verified.
- Case studies clearly distinguish the owner's work from team work.
- All content is approved for public disclosure.
- Navigation, links, responsive layout, keyboard access, and accessibility have
  been checked.
- Game demos and other artifacts are labeled accurately and work as described.
- The README setup and deployment instructions match the actual implementation.
