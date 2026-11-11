# Øvelse 1 · Nyt projekt fra skabelonen 🛠️ (20 min)

Mål: Tag imod GoldenBase-løsningen, tilret den og importér den som dit eget projekt.

## 1. Eksportér GoldenBase fra dev (én gang pr. facilitator)

```bash
pac solution export --name GoldenBase --path ./artifacts/GoldenBase.zip
```

## 2. Klone den til et nyt projekt (deltagerne gør her)

```bash
# 1) Kopiér skabelonrepoets struktur til dit projekt
git clone https://github.com/PrimeLarsen/golden-repo-for-power-platform.git mitprojekt
cd mitprojekt

# 2) Opret din egen solution i dev med projektnavn
pac solution create --name "ProjektKundportal" --publisher-name "Golden" --publisher-prefix gld

# 3) Eksportér GoldenBase og pak den UD til læsning (til senere øvelser)
pac solution export --name GoldenBase --path ./artifacts/
pac solution unpack --zipfile ./artifacts/GoldenBase.zip --folder ./src/GoldenBase --allowDelete
```

## 3. Tilret dit projekt i Maker Portal

1. Åbn **Solutions → ProjektKundportal**
2. Tilføj en ny canvas-app: `appKundportal`
3. Brug komponentbiblioteket fra GoldenBase — indsæt en header og en knap fra biblioteket (ikke byg selv!)
4. Tilføj en ny tabel `gldOrdre` med kolonnerne `gldOrdrenummer`, `gldOrdrestatus`, `gldOrdredato`

## 4. Eksportér dit projekt ind i repoet (ALM-flowet)

```bash
pac solution export --name ProjektKundportal --path ./artifacts/ProjektKundportal.zip
pac solution unpack --zipfile ./artifacts/ProjektKundportal.zip --folder ./src/ProjektKundportal --allowDelete
git add .
git commit -m "feat: projekt Kundportal baseret på GoldenBase"
```

## ✅ Tjek

- [ ] Din solution ligger i dev og afhænger af GoldenBase
- [ ] Din app bruger komponentbibliotekets komponenter
- [ ] `src/`-mappen i repoet har begge solutions pakket ud

**Faldgrube:** Eksporter du en solution, der stadig er unmanaged i dev, får du unmanaged zip — fint til dev, men pipeline skal bygge managed til test/prod.
