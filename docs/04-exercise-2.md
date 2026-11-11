# Exercise 2 · Design rules + Solution Checker ✅ (20 min)

Goal: Apply the rules and run quality control like a build gate.

## 1. Review your app against DESIGN-RULES.md

Checklist — find at least 2 things to fix:

- [ ] Colors match the palette (primary `#0B5394`, background `#F5F5F5` ...)
- [ ] Font is Segoe UI and text sizes follow the library
- [ ] Physical names: `gldOrder`, `gldOrderStatus` — no spaces
- [ ] Flows use connection references — not inline connections
- [ ] Environment variables exist for anything environment-specific
- [ ] The app is responsive (flexible containers)

## 2. Run the Solution Checker

```bash
pac solution check --path ./artifacts/ProjectCustomerPortal.zip
```

Read the output. Result categories:

| Severity | Meaning | Action |
|---|---|---|
| Critical | Quality or security defect | Must fix |
| High/Important | Should fix | Fix if possible |
| Low/Information | Suggested improvement | Evaluate |

## 3. Fix at least one critical/high issue and re-run

The loop is the point:
```bash
# fix in the Maker Portal / the src folder
pac solution export --name ProjectCustomerPortal --path ./artifacts/
pac solution unpack --zipfile ./artifacts/ProjectCustomerPortal.zip --folder ./src/ProjectCustomerPortal --allowDelete
pac solution check --path ./artifacts/ProjectCustomerPortal.zip
```

## ✅ Checklist

- [ ] You found and fixed at least 1–2 design-rule violations
- [ ] Solution Checker runs with 0 criticals

**Plenary discussion:** Which rules would your organization struggle most to enforce — and why? (SPOILER: it's always naming 🙃)
