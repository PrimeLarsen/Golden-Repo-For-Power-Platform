# 02 · What is a Golden Solution? 🏆

A **golden solution** is an empty but well-built base: all the boring stuff that has to be done right in every project is already done.

## What's inside GoldenBase?

| Category | Contents |
|---|---|
| **Design system** | Component library with buttons, headers, cards, icons, color variables |
| **Configuration** | Environment variables (API URL, SharePoint site) and connection references |
| **Data model** | Shared tables: organizations, users, log |
| **Utilities** | Reusable flows: error handling, notifications, audit logging |
| **App shell** | Canvas app with navigation, header, and an "empty" form |

## The flow: from template to project

```mermaid
flowchart LR
    A[GoldenBase template\n(this repo)] --> B[Exercise 1:\nclone copy to dev]
    B --> C[Build the project\non top of the base]
    C --> D[Exercise 2:\nChecker + design rules]
    D --> E[Exercise 3:\nCI/CD pipeline]
    E --> F[Test/Prod\n(managed)]
```

## Why not just copy the app?

- Copy an app and you duplicate bugs — and design drift.
- Reference a managed base and every project inherits fixes in one update.
- Solutions are the ALM unit: export, import, deployment — it's all about solutions, not apps.

## The principle

> **Build the box once. Live in the box. Only build what's unique to the project.**
