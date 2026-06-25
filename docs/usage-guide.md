# Usage Guide

## Purpose

This guide explains how to use Agent Housekeeper in another repo.

## Step 1: Add Required Root Files

```text
README.md
ABOUT.md
PRD.md
LICENSE
repo-manifest.md
release-ledger.md
```

## Step 2: Add Housekeeper Folder

Copy or reference:

```text
agents/housekeeper/
```

## Step 3: Add Feature Ledger

Create:

```text
features/README.md
features/ledger.md
features/tickets/
```

## Step 4: Point The Agent To First Read

Start the agent with:

```text
agents/housekeeper/system-prompt/00-core-system-prompt.md
```

Then load the firing order.

## Step 5: Run A Repo Audit

Use:

```text
agents/housekeeper/templates/repo-audit-template.md
```

## Step 6: Validate

Use:

```text
agents/housekeeper/templates/validation-report-template.md
```
