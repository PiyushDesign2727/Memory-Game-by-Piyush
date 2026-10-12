# AI Product Manager Portfolio — Starter

A starter repository for building a clear, evidence-based portfolio that shows
how you identify product problems, make decisions, collaborate with engineering
and design, and evaluate AI-enabled experiences.

> **Current status:** This repository contains the portfolio setup guidance
  plus two standalone browser-game projects. It is not yet a completed portfolio
  website. Replace bracketed placeholders with your verified information before
  sharing it with employers or the public.

## Portfolio goals

Use the portfolio to help a hiring team quickly understand:

- What kinds of product problems you work on.
- How you turn user and business needs into a product strategy.
- How you prioritize, define, and ship solutions with a team.
- How you assess AI use cases, quality, risk, and human oversight.
- What outcomes you achieved and how those outcomes were measured.

The portfolio should show the work and reasoning behind results—not just a
collection of polished screens or AI terminology.

## Recommended portfolio sections

1. **Home:** Your name, target role, concise value proposition, and links to
   your strongest case studies.
2. **About:** Your verified background, product domains, working style, and
   areas of interest.
3. **Case studies:** Two or three substantial examples, each with the problem,
   evidence, decisions, execution, and outcomes.
4. **AI product work:** Relevant AI use cases with evaluation, limitations,
   privacy, safety, and human-review considerations. If you do not yet have
   shipped AI-product experience, label experiments and proposals accurately.
5. **Artifacts:** Selected PRDs, prototypes, research summaries, roadmaps, or
   evaluation plans that you are authorized to share.
6. **Resume and contact:** A current resume and professional contact links you
   have chosen to publish.

## Case-study structure

For each project, document:

- **Summary:** Project, role, timeframe, team, and status (shipped, in progress,
  prototype, or proposal).
- **Problem:** The user need and business context; explain how the problem was
  discovered and validated.
- **Evidence:** Research, support themes, analytics, experiments, or other
  sources, with dates and limitations where relevant.
- **Goal and success measures:** Baseline, target, metric definitions, and
  guardrails. State when values are estimates or unavailable.
- **Options and decisions:** Alternatives considered, prioritization rationale,
  trade-offs, and what you decided not to do.
- **Solution and delivery:** User experience, scope, requirements, collaboration,
  launch approach, and your specific contribution.
- **AI considerations (when applicable):** Why AI is appropriate, model or
  system behavior at a high level, evaluation data and methods, failure modes,
  privacy and safety boundaries, and human oversight.
- **Outcome:** Measured results, measurement period, attribution limits, and
  what changed after launch. Never invent impact numbers.
- **Reflection:** What you learned, what you would change, and follow-up work.

## Existing project material

The repository currently includes:

- [`memory-game.html`](memory-game.html): A standalone Memory Game with a
  persistent light/dark theme, keyboard interaction, scores, and two board
  sizes. This can be presented as a product/design/implementation case study
  only when your actual contribution and decisions are documented.
- [`snake.html`](snake.html): A standalone Snake game with keyboard and touch
  controls, pause/resume, scoring, and a saved best score.
- [`PRD_dark_theme.md`](PRD_dark_theme.md) and [`PRD_snake.md`](PRD_snake.md):
  product-requirement examples for the two games.
- [`context.md`](context.md): Guidance for contributors and AI tools working on
  the portfolio.

These games are not AI products by themselves. Do not describe them as
AI-powered or claim outcomes, research, leadership, or personal contributions
that have not been verified.

## Getting started

### 1. Add your verified profile

Replace these placeholders when you are ready:

- `[YOUR NAME]`
- `[TARGET ROLE OR PRODUCT DOMAIN]`
- `[SHORT, EVIDENCE-BASED VALUE PROPOSITION]`
- `[PROFESSIONAL EMAIL OR CONTACT LINK]`
- `[LINKEDIN URL]`
- `[RESUME LOCATION OR LINK]`

Use only information you want to make public. Do not add private employer,
customer, or user data.

### 2. Choose your case studies

Select work that demonstrates different strengths, for example discovery and
prioritization, delivery and cross-functional leadership, or AI evaluation and
responsible launch. For each project, confirm that you have permission to share
the content and that all metrics and dates are accurate.

### 3. Create portfolio pages

The repository is currently a small set of standalone HTML pages; the portfolio
site structure below is a suggested next step, not existing code:

```text
index.html
about.html
case-studies/
  case-study-template.md
  project-one.md
assets/
  images/
  styles.css
resume/
  resume.pdf
```

Start with a responsive static site unless your needs require a framework or
backend. Keep the game demos independently playable. Do not commit credentials,
private data, or a resume containing details you do not intend to publish.

### 4. Review before publishing

- Verify names, titles, dates, roles, metrics, and links.
- Mark prototypes and proposals clearly; distinguish them from shipped work.
- Remove confidential material and obtain permission for third-party work.
- Check keyboard access, mobile layout, contrast, and link behavior.
- Test the site locally, then deploy it to a static host such as GitHub Pages
  after choosing the final site structure.

## Run the current game demos

Open either HTML file directly in a modern browser, or optionally serve the
repository:

```bash
python -m http.server 8000
```

Then open:

- <http://localhost:8000/memory-game.html>
- <http://localhost:8000/snake.html>

## Working with AI tools

Use [`context.md`](context.md) as the source of truth for the portfolio's
purpose, content rules, and implementation guidance. AI can help structure,
edit, and critique material, but you are responsible for verifying every claim,
metric, citation, and public disclosure.

## Repository

This starter is hosted at
<https://github.com/PiyushDesign2727/Memory-Game-by-Piyush>.
