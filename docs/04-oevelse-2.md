# Øvelse 2 · Designregler + Solution Checker ✅ (20 min)

Mål: Anvend reglerne og kør kvalitetskontrol som en (bygge)kontrol.

## 1. Gennemgå din app mod DESIGN-RULES.md

Tjekliste — find mindst 2 ting at rette:

- [ ] Farver matcher paletten (primær `#0B5394`, baggrund `#F5F5F5` ...)
- [ ] Font er Segoe UI og tekststørrelser følger biblioteket
- [ ] Fysiske navne: `gldOrdre`, `gldOrdrestatus` — ingen mellemrum
- [ ] Flows bruger connection references — ikke inline-connections
- [ ] Miljøvariabler findes til alt miljøafhængigt
- [ ] Appen er responsive (flexible containers)

## 2. Kør Solution Checker

```bash
pac solution check --path ./artifacts/ProjektKundportal.zip
```

Læs outputtet. Typer af resultater:

| Alvorlighed | Betydning | Handling |
|---|---|---|
| Critical | Kvalitets- eller sikkerhedsfejl | Skal rettes |
| High/Important | Burde rettes | Ret hvis muligt |
| Low/Information | Foreslået forbedring | Vurder |

## 3. Ret mindst én critical/high-fejl og kør igen

Loopet er pointen:
```bash
# ret i Maker Portal / src-mappen
pac solution export --name ProjektKundportal --path ./artifacts/
pac solution unpack --zipfile ./artifacts/ProjektKundportal.zip --folder ./src/ProjektKundportal --allowDelete
pac solution check --path ./artifacts/ProjektKundportal.zip
```

## ✅ Tjek

- [ ] Du har fundet og rettet mindst 1-2 designbrud
- [ ] Solution Checker kører med 0 criticals

**Diskussion i plenum:** Hvilke regler ville jeres organisation have sværest ved at håndhæve — og hvorfor? (SPOILER: altid navngivning 🙃)
