# Repo Transformation Guide

## Purpose

This guide explains how to reorganize another repo into a Housekeeper-style repo.

## Target Structure

```text
project-root/
├── README.md
├── ABOUT.md
├── PRD.md
├── LICENSE
├── repo-manifest.md
├── release-ledger.md
├── docs/
├── examples/
├── features/
│   ├── README.md
│   ├── ledger.md
│   └── tickets/
├── agents/
│   └── housekeeper/
└── tests/
```

## Steps

1. Inspect the repo.
2. Identify the project purpose.
3. Add root project files.
4. Add feature ledger.
5. Add Housekeeper folder.
6. Add docs and examples folders.
7. Add tests folder.
8. Update README.
9. Validate the repo.

## Rule

Do not destroy old structure too fast.

Add the new structure first, then move or link old files carefully.
