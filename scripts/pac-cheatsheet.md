# PAC CLI — cheat sheet 📋

All the workshop commands in one place.

## Auth

```bash
pac auth create --url https://yourorg.crm4.dynamics.com   # sign in
pac auth list                                            # list connections
pac auth select --index 2                                # switch active
```

## Solutions — the ALM flow

```bash
pac solution list                                        # list all in the environment
pac solution create --name X --publisher-name Y --publisher-prefix z
pac solution export --name X --path ./artifacts/          # export as zip
pac solution unpack --zipfile X.zip --folder ./src/X --allowDelete
pac solution pack --folder ./src/X --zipfile X.zip --managed true
pac solution import --file X.zip                          # import it back
pac solution check --path X.zip                           # Solution Checker
```

## Help

```bash
pac help
pac solution help
```

> **Tip:** `pac` can be used in GitHub Actions via `microsoft/powerplatform-actions` — the same commands, just in a pipeline.
