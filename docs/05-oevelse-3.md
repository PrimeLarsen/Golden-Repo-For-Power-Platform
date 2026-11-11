# Øvelse 3 · CI-pipeline med GitHub Actions 🚀 (20 min, valgfri)

Mål: Automatisér ALM-flowet, så mennesker ikke skal huske eksport/import.

## 1. Kig på workflow-filen

Åbn `.github/workflows/solution-alignment.yml` i dette repo. Den viser to klassiske jobs:

1. **Export & commit** — automatisk eksport af solution fra dev, unpack og commit til repo.
2. **Build & deploy** — pack af `src/`-mappen til managed zip og import til test, + Solution Checker som gate.

## 2. Prøv den (hvis I har et fælles dev-environment)

1. Opret environments i GitHub repoet: **Settings → Environments** — eller brug secrets:
   - `POWERPLATFORM_URL` (test-environmentets URL)
   - `POWERPLATFORM_TENANT_ID`, `POWERPLATFORM_CLIENT_ID`, `POWERPLATFORM_CLIENT_SECRET` (service principal — opret via `pac admin` eller Entra ID app registration)
2. Kør workflowet manuelt: **Actions → Export solution → Run workflow**
3. Se filerne blive commitet og solutionen blive importeret til test

## 3. Vigtig viden

- Pipelinen bruger [microsoft/powerplatform-actions](https://github.com/microsoft/powerplatform-actions) — de officielle GitHub Actions til Power Platform.
- Service principal > personlige konti i pipelines. Altid.
- Import til prod sker typisk ikke via GitHub direkte — brug Power Platform Pipelines (platformens indbyggede) til prod-deploy.

## ✅ Tjek

- [ ] Du forstår hvad de to jobs gør
- [ ] Du ved hvilke secrets der skal til for at kører det selv

**Take-away:** I dag gjorde i det manuelt. Pipelinen gør det samme — hver gang, uden at nogen glemmer Solution Checker.
