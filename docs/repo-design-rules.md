# Repo Design Rules

## Purpose

This file defines the repo design rules that Agent Housekeeper must follow.

These rules come from the Motif repo pattern.

## Core Rule

A repo should be organized like a living knowledge system.

It should be easy for a human to read and easy for an AI agent to load, search, chunk, index, and maintain.

## Required Root Files

Every Housekeeper-style repo should include:

```text
README.md
ABOUT.md
PRD.md
LICENSE
repo-manifest.md
release-ledger.md
```

## Required Folders

Every Housekeeper-style repo should include:

```text
agents/
agents/housekeeper/
agents/housekeeper/system-prompt/
agents/housekeeper/templates/
docs/
examples/
features/
features/tickets/
obsidian/
obsidian/journal/
tests/
```

## Root File Duties

## README.md

The front door.

It should explain what the repo is, where to start, and which files matter.

## ABOUT.md

The identity file.

It should explain the deeper meaning and purpose of the repo.

## PRD.md

The product requirements document.

It should explain what the repo is supposed to become.

## LICENSE

The legal license file.

It should always exist and remain visible.

## repo-manifest.md

The inventory.

It should list the major files, folders, and Housekeeper duties.

## release-ledger.md

The milestone memory.

It should track important versions and project states.

## Folder Duties

## agents/

Stores agent definitions, system prompts, templates, and operating rules.

## docs/

Stores product, process, and technical documentation.

## examples/

Stores sample repo structures and practical examples.

## features/

Stores the feature ledger and small Markdown feature tickets.

## obsidian/

Stores wiki-style knowledge notes.

## obsidian/journal/

Stores decision history and project memory.

## tests/

Stores validation notes and future test plans.

## Micro-Document Rule

Prefer small, focused Markdown files.

One concept should usually become one file.

## Ledger Rule

If a buildable idea appears, create a feature ticket and update the feature ledger.

## Journal Rule

If a decision changes the project memory, add a journal entry.

## Manifest Rule

If a major file or folder is added, update the repo manifest.

## Release Rule

If a major project state changes, update the release ledger.

## Firing Order Rule

Agent instruction files should have a clear load order.

The first-read folder is:

```text
agents/housekeeper/system-prompt/
```

## Validation Rule

The Housekeeper should always report what is complete, what needs review, and what is missing.
