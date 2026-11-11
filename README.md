# Golden Repo — Power Platform 🏆

Hands-on workshop (60–90 min): **Build a "Golden Repo" with solution templates, design rules, and cross-project reuse.**

Audience: Power Platform developers (primarily) and makers who want structure, reuse, and quality in their projects.

## Why a Golden Repo?

Without templates, every project starts from zero — new colors, new names, new (bad) habits. With a Golden Repo you get:

- **Speed**: New project = clone the template, unpack, build on top. Hours saved every time.
- **Quality**: Design rules, naming, and the Solution Checker are "baked in" from day one.
- **Reuse**: Component libraries, environment variables, and connections are defined once.
- **ALM**: The same export/import flow in every project, ready for CI/CD.
- **AI-ready**: Agents read the rules files and enforce the standard for you 🤖

## Repo overview

| Path | Contents |
|---|---|
| DESIGN-RULES.md | Design & naming rules (our "law") |
| AGENTS.md | 🤖 Operating manual for AI coding agents |
| docs/01-setup.md | Setup: PAC CLI, auth, cloning the repo |
| docs/02-golden-template.md | What's inside the golden solution template? |
| docs/03-exercise-1.md | Exercise 1: New project from the template |
| docs/04-exercise-2.md | Exercise 2: Design rules + Solution Checker |
| docs/05-exercise-3.md | Exercise 3 (optional): CI pipeline with GitHub Actions |
| docs/06-cicd-and-branches.md | 📖 Read-after: CI/CD & branching basics |
| docs/07-agentic-development.md | 🤖 Demo: AI agents + the golden repo |
| scripts/pac-cheatsheet.md | The PAC CLI commands you'll use today |
| .github/copilot-instructions.md | 🤖 Rules that GitHub Copilot follows automatically |
| .github/workflows/ | ALM pipeline + design rules PR review bot |

## Agenda (60–90 min)

1. **Intro** (10 min) — why reuse beats reinvention: [docs/02](docs/02-golden-template.md)
2. **Setup** (10 min) — PAC CLI + auth: [docs/01](docs/01-setup.md)
3. **Exercise 1** (20 min) — new project from the golden template: [docs/03](docs/03-exercise-1.md)
4. **Exercise 2** (20 min) — design rules + Solution Checker: [docs/04](docs/04-exercise-2.md)
5. **Exercise 3** (20 min, optional) — CI pipeline: [docs/05](docs/05-exercise-3.md)
6. **Wrap-up** (5–10 min) — how do you take this home? Discussion. Bonus: [AI agents demo](docs/07-agentic-development.md)

📖 **Homework / further reading:** [CI/CD & branches](docs/06-cicd-and-branches.md) · [Agentic development](docs/07-agentic-development.md)

## Prerequisites

- A Power Platform developer license (and access to a dev environment)
- Git installed
- Power Platform CLI (PAC) — see [docs/01](docs/01-setup.md)

## The golden rule

> *"Everything that repeats belongs in the golden repo. Everything you hardcode will come back to haunt you."*
