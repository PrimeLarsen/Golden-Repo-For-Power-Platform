# Copilot Instructions — Golden Repo

This file is read automatically by GitHub Copilot when generating code and working on issues in this repo.

## What this repo is

A Golden Repo for Power Platform: solution templates, design rules, and ALM automation
that teams clone to start new Power Platform projects. You (the agent) exist to keep
projects aligned with the golden standard.

## Non-negotiable rules (from DESIGN-RULES.md)

Read DESIGN-RULES.md before generating anything. Key points:

- **Naming**: physical names follow the conventions — app<CustomerPortal>, mdd<...>, flow<...>, tables/columns prefixed gld, environment variables var<...>. No spaces, no special characters, no non-ASCII in physical names.
- **Colors**: use the palette exactly — Primary #0B5394, Secondary #3D85C6, Background #F5F5F5, Text #202124, Success #2E7D32, Warning #F9A825, Error #C5221F.
- **Font**: Segoe UI. Always.
- **Components**: reuse the GoldenBase component library — never invent new button/header/card variants.
- **Configuration**: environment variables for anything environment-specific; connection references for all connections. Never hardcode URLs, site names, or credentials.
- **Solutions**: project solutions only contain project-specific content. Reference GoldenBase — never copy from it.
- **Managed in prod**: pipelines must deploy managed solutions. Unmanaged stays in dev.

## ALM commands you'll need

```bash
pac solution export --name <Solution> --path ./artifacts/        # export from dev
pac solution unpack --zipfile <X>.zip --folder ./src/<X> --allowDelete
pac solution pack --folder ./src/<X> --zipfile <X>.zip --managed true
pac solution check --path ./artifacts/<X>.zip                     # quality gate
```

## How to work in this repo

1. Read DESIGN-RULES.md and the relevant docs/ file first.
2. Solutions live unpacked in src/<SolutionName> — never edit generated files by hand unless unpacked consistently.
3. Prefer small, reviewable changes: one solution change per PR.
4. After any solution change, run the export → unpack → check loop before committing.
5. If a requirement conflicts with a design rule, follow the rule and note the conflict — don't silently improvise.

## Tone of the repo

Practical, minimal, reusable. Comments and docs in English. When in doubt: consistency beats cleverness.
