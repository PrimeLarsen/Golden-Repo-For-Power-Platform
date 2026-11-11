# 01 · Klargøring 🔧

Mål: Alle har PAC CLI kørende og er logget ind på deres dev-environment.

## 1. Installer Power Platform CLI

Windows:
```powershell
winget install Microsoft.PowerAppsCLI
```

macOS / Linux:
```bash
dotnet tool install --global Microsoft.PowerAppsCLI.Tool
```

(Kommandonavnet er `pac` i begge tilfælde.)

## 2. Log ind på dit dev-environment

```bash
pac auth create --url https://ditorg.crm4.dynamics.com
```

Tjek at du er forbundet:
```bash
pac auth list
```

## 3. Klone dette repo

```bash
git clone https://github.com/PrimeLarsen/golden-repo-for-power-platform.git
cd golden-repo-for-power-platform
```

## 4. Tjek at alt virker

```bash
pac solution list
```

Hvis du kan se dine solutions — klar! 👌

**Faldgrube:** Hvis `crm4` ikke passer, tjek hvilken region dit environment ligger i (crm4 = Europa).
