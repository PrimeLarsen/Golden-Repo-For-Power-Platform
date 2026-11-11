# Exercise 1 · New project from the template 🛠️ (20 min)

Goal: Take the GoldenBase solution, adapt it, and import it as your own project.

## 1. Export GoldenBase from dev (once per facilitator)

```bash
pac solution export --name GoldenBase --path ./artifacts/GoldenBase.zip
```

## 2. Clone it into a new project (participants start here)

```bash
# 1) Copy the template repo structure to your project
git clone https://github.com/PrimeLarsen/Golden-Repo-For-Power-Platform.git myproject
cd myproject

# 2) Create your own solution in dev with your project name
pac solution create --name "ProjectCustomerPortal" --publisher-name "Golden" --publisher-prefix gld

# 3) Export GoldenBase and unpack it for reading (for later exercises)
pac solution export --name GoldenBase --path ./artifacts/
pac solution unpack --zipfile ./artifacts/GoldenBase.zip --folder ./src/GoldenBase --allowDelete
```

## 3. Adapt your project in the Maker Portal

1. Open **Solutions → ProjectCustomerPortal**
2. Add a new canvas app: `appCustomerPortal`
3. Use the component library from GoldenBase — insert a header and a button from the library (don't build your own!)
4. Add a new table `gldOrder` with the columns `gldOrderNumber`, `gldOrderStatus`, `gldOrderDate`

## 4. Export your project into the repo (the ALM flow)

```bash
pac solution export --name ProjectCustomerPortal --path ./artifacts/ProjectCustomerPortal.zip
pac solution unpack --zipfile ./artifacts/ProjectCustomerPortal.zip --folder ./src/ProjectCustomerPortal --allowDelete
git add .
git commit -m "feat: CustomerPortal project based on GoldenBase"
```

## ✅ Checklist

- [ ] Your solution exists in dev and depends on GoldenBase
- [ ] Your app uses the component library's components
- [ ] The `src/` folder in the repo has both solutions unpacked

**Pitfall:** Exporting a solution that is still unmanaged in dev gives you an unmanaged zip — fine for dev, but the pipeline must build managed for test/prod.
