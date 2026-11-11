# Exercise 3 · CI pipeline with GitHub Actions 🚀 (20 min, optional)

Goal: Automate the ALM flow so humans don't have to remember export/import.

## 1. Look at the workflow file

Open `.github/workflows/solution-alignment.yml` in this repo. It shows two classic jobs:

1. **Export & commit** — automatic export of the solution from dev, unpack, and commit to the repo.
2. **Build & deploy** — pack the `src/` folder into a managed zip and import it into test, plus the Solution Checker as a gate.

## 2. Try it (if you share a dev environment)

1. Create environments in the GitHub repo: **Settings → Environments** — or use repository secrets:
   - `POWERPLATFORM_URL` (the test environment URL)
   - `POWERPLATFORM_TENANT_ID`, `POWERPLATFORM_CLIENT_ID`, `POWERPLATFORM_CLIENT_SECRET` (service principal — create via `pac admin` or an Entra ID app registration)
2. Run the workflow manually: **Actions → Export solution → Run workflow**
3. Watch the files get committed and the solution imported into test

## 3. Key knowledge

- The pipeline uses [microsoft/powerplatform-actions](https://github.com/microsoft/powerplatform-actions) — the official GitHub Actions for Power Platform.
- Service principal > personal accounts in pipelines. Always.
- Prod deploys usually don't go through GitHub directly — use Power Platform Pipelines (the platform's built-in feature) for prod deployments.

## ✅ Checklist

- [ ] You understand what the two jobs do
- [ ] You know which secrets are needed to run it yourself

**Take-away:** Today you did it manually. The pipeline does the same thing — every time, and nobody forgets the Solution Checker.
