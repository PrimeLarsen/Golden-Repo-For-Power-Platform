# 01 · Setup 🔧

Goal: Everyone has the PAC CLI running and is signed in to their dev environment.

## 1. Install the Power Platform CLI

Windows:
```powershell
winget install Microsoft.PowerAppsCLI
```

macOS / Linux:
```bash
dotnet tool install --global Microsoft.PowerAppsCLI.Tool
```

(The command is `pac` in both cases.)

## 2. Sign in to your dev environment

```bash
pac auth create --url https://yourorg.crm4.dynamics.com
```

Verify you're connected:
```bash
pac auth list
```

## 3. Clone this repo

```bash
git clone https://github.com/PrimeLarsen/Golden-Repo-For-Power-Platform.git
cd Golden-Repo-For-Power-Platform
```

## 4. Check that everything works

```bash
pac solution list
```

If you can see your solutions — you're ready! 👌

**Pitfall:** If `crm4` doesn't match, check which region your environment is in (crm4 = Europe).
