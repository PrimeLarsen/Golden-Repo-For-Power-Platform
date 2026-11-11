# 07 · Agentic development — let AI carry the boilerplate 🤖

*(Supporting material + demo. The pitch: the agent follows the repo's rules so the developer can focus on requirements and creativity.)*

## The idea in one sentence

A golden repo gives AI agents everything they need to work *the right way*: rules, conventions, structure, and quality gates — so "vibe coding" becomes **"governed coding"**.

## Why this repo makes AI better

Without context, an AI agent guesses. With this repo, it knows:

| What the agent reads | What it gets |
|---|---|
| DESIGN-RULES.md | Naming, colors, components, configuration patterns |
| AGENTS.md | How to work: repo map, rules, definition of done |
| .github/copilot-instructions.md | Copilot-specific version of the same rules |
| src/ (unpacked solutions) | Real examples of "how we do things" |
| PR review bot (workflows) | Automatic design-rules checklist on every PR |

This is the pattern known as **context engineering**: the golden repo isn't just a template for humans — it's the *operating manual for your AI agents*.

## Agentic levels in GitHub

1. **Inline suggestions** — Copilot autocompletes formulas and Power Fx in VS Code / maker tools.
2. **Chat mode** — ask questions grounded in the repo ("what naming should this table follow?").
3. **Coding agent** — assign an issue to **@copilot** and it creates a branch, writes the change, and opens a PR — *following copilot-instructions.md and DESIGN-RULES.md*.
4. **PR review** — Copilot reviews PRs when enabled (repo Settings → Copilot), plus this repo's own design-rules checklist bot.

## Try it yourself (post-workshop)

1. Open a GitHub issue: *"Add a gldCustomer table with gldCustomerName, gldEmail, gldPhone following DESIGN-RULES.md."*
2. Assign the issue to @copilot (the coding agent must be enabled for the repo/organization).
3. Watch it create a PR that follows the naming conventions — because the instructions files told it to.
4. Notice the PR review bot commenting the design checklist.
5. You review the *requirements* — the agent already handled the *conventions*.

## Prompts that work well with a golden repo

- *"Follow DESIGN-RULES.md and draft a component list for a customer portal header."*
- *"Refactor this flow description to use connection references and environment variables."*
- *"Check src/ for naming violations against DESIGN-RULES.md and list findings."*
- *"Write release notes for GoldenBase v1.3 based on the recent commits."*

## The value pitch (for the skeptics)

> The agent doesn't replace the developer — it replaces the **boring parts**: remembering conventions, wiring configuration, writing boilerplate, enforcing the checklist. The developer keeps the two things AI is worst at: **deciding what to build, and caring that it's good.**

## Where to go deeper

- [Copilot coding agent documentation](https://docs.github.com/en/copilot/concepts/agents/coding-agent)
- [Best practices for Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/best-practices-for-using-copilot-to-work-on-tasks-and-review-code)
- [AGENTS.md convention](https://agents.md/)
