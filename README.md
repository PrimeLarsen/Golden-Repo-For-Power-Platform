# Golden Repo — Power Platform 🏆

Hands-on workshop (60–90 min): **Byg et "Golden Repo" med solution templates, designregler og genbrug på tværs af projekter.**

Målgruppe: Power Platform-udviklere (primært) og makers, der vil have struktur, genbrug og kvalitet i deres projekter.

## Hvorfor et Golden Repo?

Uden skabeloner starter hvert projekt fra nul — nye farver, nye navne, nye (dårlige) vaner. Med et Golden Repo får I:

- **Fart**: Nyt projekt = klone skabelon, pakke ud, bygge videre. Timer sparet hver gang.
- **Kvalitet**: Designregler, navngivning og Solution Checker er "bagt ind" fra dag ét.
- **Genbrug**: Komponentbiblioteker, miljøvariabler og connections defineres én gang.
- **ALM**: Samme eksport/import-flow i alle projekter, klar til CI/CD.

## Repo-oversigt

| Sti | Indhold |
|---|---|
| `DESIGN-RULES.md` | Design- og navngivningsregler (vores "lo") |
| `docs/01-klargoring.md` | Opsætning: PAC CLI, auth, klone repo |
| `docs/02-golden-template.md` | Hvad indeholder golden solution-skabelonen? |
| `docs/03-oevelse-1.md` | Øvelse 1: Nyt projekt fra skabelonen |
| `docs/04-oevelse-2.md` | Øvelse 2: Designregler + Solution Checker |
| `docs/05-oevelse-3.md` | Øvelse 3 (valgfri): CI-pipeline med GitHub Actions |
| `scripts/pac-cheatsheet.md` | PAC CLI-kommandoer du skal bruge i dag |
| `.github/workflows/` | Eksempel på ALM-pipeline til løbende brug |

## Agenda (60–90 min)

1. **Intro** (10 min) — hvorfor genbrug beats genopfindelse: [docs/02](docs/02-golden-template.md)
2. **Klargøring** (10 min) — PAC CLI + auth: [docs/01](docs/01-klargoring.md)
3. **Øvelse 1** (20 min) — nyt projekt fra golden template: [docs/03](docs/03-oevelse-1.md)
4. **Øvelse 2** (20 min) — designregler + Solution Checker: [docs/04](docs/04-oevelse-2.md)
5. **Øvelse 3** (20 min, valgfri) — CI-pipeline: [docs/05](docs/05-oevelse-3.md)
6. **Wrap-up** (5–10 min) — hvordan tager I dette med hjem? Diskussion.

## Forudsætninger

- En Power Platform-udviklerlicens (og adgang til et dev-environment)
- Git installeret
- Power Platform CLI (PAC) — se [docs/01](docs/01-klargoring.md)

## Huskereglen

> *"Alt hvad der gentager sig, hører hjemme i golden repo. Alt hvad du hardcoder, kommer til at genere dig senere."*
