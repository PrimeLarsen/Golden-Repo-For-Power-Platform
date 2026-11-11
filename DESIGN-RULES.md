# Designregler — vores "golden lo" 📐

Disse regler gælder for alt, der bygges på tværs af projekter. De er ikke eksklusive — de er minimumsstandarden.

## 1. Navngivning

| Objekt | Regel | Eksempel |
|---|---|---|
| Publisher | Fast virksomhedspublisher med prefix `gld` | `gld` |
| Løsning (solution) | `GoldenBase` (skabelon) / `Projektnavn_Feature` | `Kundportal_Bestilling` |
| Canvas-app | `app` + domæne | `appKundportal` |
| Model-driven | `mdd` + domæne | `mddKundportal` |
| Flow | `flow` + proces | `flowSendOrdrebekraftelse` |
| Dataverse-tabel | prefix + ental, CamelCase | `gldOrdre` |
| Kolonne | prefix + navn | `gldOrdrestatus` |
| Miljøvariabel | `var` + navn | `varApiUrl` |

- Fysiske navne (**Name**) er tekniske, visningsnavne (**DisplayName**) er menneskelige.
- Ingen mellemrum, æøå eller specialtegn i fysiske navne.

## 2. Solution-struktur

- **GoldenBase** (managed i prod): designsystem, komponentbibliotek, miljøvariabler, connection references, delte tabeller.
- **Projekt-solutions**: kun det specifikke projekt. Afhænger af GoldenBase — aldrig kopier indhold, altid referer.
- Ingenting bygges i **Default**-environment. Brug dedikerede dev/test/prod environments.

## 3. Visuel design (Canvas-apps)

- **Font**: Segoe UI (standard) — ingen andre fonte uden aftale.
- **Skema**: Ét farvesystem, defineret i komponentbiblioteket:
  - Primær: `#0B5394` • Sekundær: `#3D85C6` • Baggrund: `#F5F5F5` • Tekst: `#202124` • Success: `#2E7D32` • Advarsel: `#F9A825` • Fejl: `#C5221F`
- **Sizing**: Header 60px, indre margin 20px, gap mellem elementer 12px.
- **Responsive**: Altid flexible containers + formulas — aldrig fast pixel-layout på skærme.
- Knapper, headers, cards og ikoner tages fra **komponentbiblioteket** — der bygges ikke nye varianter "hovs"-kreativt.

## 4. Konfiguration

- **Miljøvariabler** til alt miljøafhængigt: API-URL'er, SharePoint-sites, parametre.
- **Connection references** til alle connections — aldrig inline-connections i flows.
- Ingen hemmeligheder, tokens eller personlige konti i flows — kun servicekonti der deles korrekt.

## 5. Kvalitetsregler

- **Solution Checker** skal køre grønt (0 critical) før import til test.
- Ingen business logic i on-change flows, hvor formel-datakilder kan bruges.
- Alt, der rører produktion, er **managed**. Unmanaged findes kun i dev.

## 6. Versionering

- Skabelonen har en version i `GoldenBase`-beskrivelsen (semver).
- Ændringer i skabelonen → pull request → review → ny version → release notes i denne repo.
