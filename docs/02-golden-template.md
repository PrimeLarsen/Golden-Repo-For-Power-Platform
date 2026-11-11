# 02 · Hvad er en Golden Solution? 🏆

En **golden solution** er en tom, men velbygget base: alt det kedelige, der skal gøres rigtigt i hvert projekt, allerede er gjort.

## Hvad indeholder GoldenBase?

| Kategori | Indhold |
|---|---|
| **Designsystem** | Komponentbibliotek med knapper, headers, cards, ikoner, farvevariabler |
| **Konfiguration** | Miljøvariabler (API-URL, SharePoint-site) og connection references |
| **Datamodel** | Fælles tabeller: organisationer, brugere, log |
| **Utilities** | Genanvendelige flows: fejlhåndtering, notifikationer, audit-log |
| **App-shell** | Canvas-app med navigation, header og "tom" formular |

## Flowet: fra skabelon til projekt

```mermaid
flowchart LR
    A[GoldenBase-skabelon\n(this repo)] --> B[Øvelse 1:\nnegotiate kopi til dev]
    B --> C[Byg projektet\novenpå basen]
    C --> D[Øvelse 2:\nChecker + designregler]
    D --> E[Øvelse 3:\nCI/CD pipeline]
    E --> F[Test/Prod\n(managed)]
```

## Hvorfor ikke bare kopiere appen?

- Kopier du en app, duplikerer du fejl — og designdrift.
- Refererer du til en managed base, arver alle projekter rettelser i én opdatering.
- Solutions er ALM-enheden: eksport, import, deployment — alt handler om solutions, ikke apps.

## Princippet

> **Byg kassen færdig én gang. Lever i kassen. Byg kun det, der er unikt for projektet.**
