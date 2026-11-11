# PAC CLI — snydeark 📋

Alle kommandoer fra workshoppen samlet ét sted.

## Auth

```bash
pac auth create --url https://ditorg.crm4.dynamics.com   # log ind
pac auth list                                          # se forbindelser
pac auth select --index 2                              # skift aktiv
```

## Solutions — ALM-flowet

```bash
pac solution list                                      # se alle i environmentet
pac solution create --name X --publisher-name Y --publisher-prefix z
pac solution export --name X --path ./artifacts/        # exportér som zip
pac solution unpack --zipfile X.zip --folder ./src/X --allowDelete
pac solution pack --folder ./src/X --zipfile X.zip --managed true
pac solution import --file X.zip                       # importér igen
pac solution check --path X.zip                         # Solution Checker
```

## Online-hjælp

```bash
pac help
pac solution help
```

> **Tip:** `pac` kan bruges i GitHub Actions via `microsoft/powerplatform-actions` — samme kommandoer, bare i pipeline.
