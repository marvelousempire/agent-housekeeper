# Shared Source Management

## Purpose

This guide explains how the Housekeeper should reduce copied standards across repos.

## Rule

When many repos need the same reusable standard, keep that standard in one source repo and let other repos reference it.

## Use Cases

- Shared agent standards
- Shared templates
- Shared prompt files
- Shared docs patterns
- Shared testing patterns

## Pattern

```text
project-repo/
├── vendor/
│   └── shared-source/
└── local-pointer/
```

## Project Duty

The local pointer folder should explain where the shared source lives and what project-specific overrides exist.

## Files To Update

- README.md
- repo-manifest.md
- release-ledger.md
- feature ledger
- journal
