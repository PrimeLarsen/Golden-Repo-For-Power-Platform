# AGENTS.md — instructions for AI coding agents

This file follows the emerging AGENTS.md convention so any capable agent (GitHub Copilot coding agent, Codex, Claude Code, Cursor, etc.) knows how to work in this repo.

## Mission

Help developers build Power Platform projects **on top of the golden standard** — so they can focus on requirements and creativity, while the agent carries boilerplate, naming, design rules, and ALM mechanics.

## Repo map

| Path | What it is |
|---|---|
| DESIGN-RULES.md | **Read this first.** The law of the land. |
| docs/ | Workshop docs: setup, exercises, CI/CD & branching basics |
| src/ | Solutions unpacked for versioning (export → unpack lives here) |
| artifacts/ | Solution zips (build output; gitignore this in real projects) |
| scripts/pac-cheatsheet.md | PAC CLI reference |
| .github/workflows/ | ALM pipeline + PR design review bot |
| .github/copilot-instructions.md | Copilot-specific guidance (same rules as here) |

## Rules for agents working here

1. **Follow DESIGN-RULES.md unconditionally.** Naming, colors, fonts, component reuse, configuration patterns.
2. **Never hardcode** environment-specific values — environment variables and connection references only.
3. **Keep ALM integrity**: any solution change must go through export → unpack (or be described so a developer can run it). If you can run pac, run pac solution check and share the results.
4. **Small PRs**: one feature or one solution change per PR, with a clear description.
5. **Don't invent new design elements** — everything visual comes from the GoldenBase component library.
6. **Say when you're unsure.** Flag conflicts with the design rules instead of improvising.

## Definition of done for a change

- [ ] Naming follows DESIGN-RULES.md
- [ ] No hardcoded config
- [ ] Component library used for all UI
- [ ] Solution exported/unpacked and committed (src/)
- [ ] Solution Checker run (0 critical)
- [ ] Docs updated if the change affects setup or workflow

## Good tasks for agents in this repo

- Scaffold new tables, columns, flows, and apps following the naming standard
- Review PRs against DESIGN-RULES.md
- Draft release notes when GoldenBase version changes
- Explain ALM mechanics to makers (use docs/ as the source of truth)
