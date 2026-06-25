---
type: load-sequence
status: active
agent: Housekeeper Agent
firing_order: 02
---

# 02 - Load Sequence

## Purpose

The Load Sequence tells the agent how to move from instructions into repo understanding.

## Sequence

```text
System Prompt Folder
→ Root Project Files
→ Agent Rules
→ Feature Ledger
→ Wiki Or Docs
→ Journal History
→ Code
→ Tests
→ Validation
```

## Root Files

Read these early:

```text
README.md
ABOUT.md
PRD.md
LICENSE
repo-manifest.md
release-ledger.md
```

## Project Memory

Then read:

```text
features/ledger.md
features/tickets/
docs/
examples/
tests/
```

## Rule

Do not update a repo before reading the files needed for the task.
