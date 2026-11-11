# Design Rules — our "golden law" 📐

These rules apply to everything built across projects. They are not exhaustive — they are the minimum standard.

## 1. Naming

| Object | Rule | Example |
|---|---|---|
| Publisher | Fixed company publisher with prefix `gld` | `gld` |
| Solution | `GoldenBase` (template) / `ProjectName_Feature` | `CustomerPortal_Ordering` |
| Canvas app | `app` + domain | `appCustomerPortal` |
| Model-driven app | `mdd` + domain | `mddCustomerPortal` |
| Flow | `flow` + process | `flowSendOrderConfirmation` |
| Dataverse table | prefix + singular, CamelCase | `gldOrder` |
| Column | prefix + name | `gldOrderStatus` |
| Environment variable | `var` + name | `varApiUrl` |

- Physical names (**Name**) are technical; display names (**DisplayName**) are human.
- No spaces, special characters, or non-ASCII letters in physical names.

## 2. Solution structure

- **GoldenBase** (managed in prod): design system, component library, environment variables, connection references, shared tables.
- **Project solutions**: only the specific project's content. They depend on GoldenBase — never copy content, always reference it.
- Nothing gets built in the **Default** environment. Use dedicated dev/test/prod environments.

## 3. Visual design (Canvas apps)

- **Font**: Segui UI — actually: **Segoe UI** (the default) — no other fonts without agreement.
- **Palette**: One color system, defined in the component library:
  - Primary: `#0B5394` • Secondary: `#3D85C6` • Background: `#F5F5F5` • Text: `#202124` • Success: `#2E7D32` • Warning: `#F9A825` • Error: `#C5221F`
- **Sizing**: header 60px, inner margin 20px, gap between elements 12px.
- **Responsive**: always flexible containers + formulas — never fixed pixel layout on screens.
- Buttons, headers, cards, and icons come from the **component library** — no improvised new variants.

## 4. Configuration

- **Environment variables** for anything environment-specific: API URLs, SharePoint sites, parameters.
- **Connection references** for all connections — never inline connections in flows.
- No secrets, tokens, or personal accounts in flows — only properly shared service accounts.

## 5. Quality rules

- **Solution Checker** must run green (0 critical) before importing to test.
- No business logic in on-change flows where formula data sources can do the job.
- Everything touching production is **managed**. Unmanaged exists only in dev.

## 6. Versioning

- The template has a version in the `GoldenBase` description (semver).
- Template changes → pull request → review → new version → release notes in this repo.
