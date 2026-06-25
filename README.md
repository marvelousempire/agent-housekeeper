# Agent Housekeeper

**Keep the house clean. Keep the memory clear. Keep the repo ready.**

Agent Housekeeper is a reusable repo-management agent standard.

It defines how an AI agent should act as a project housekeeper: reading the repo, preserving founder intent, organizing docs, maintaining README files, tracking features, creating journals, keeping release memory, validating changes, and preparing the repo for RAG, Obsidian, and AI-assisted workflows.

## Purpose

This repo is the reusable standard for Housekeeper Agents.

A project can point an agent to this repo so the agent understands how to set up and maintain a clean, modular, wiki-ready, RAG-ready project structure.

## Core Idea

A repo is a house.

The Housekeeper Agent keeps the house organized.

It knows which files matter, which folders must exist, which ledgers must be updated, and which rules should fire first.

## First Read

The agent should start here:

```text
agents/housekeeper/system-prompt/00-core-system-prompt.md
```

Then follow:

```text
agents/housekeeper/system-prompt/01-firing-order.md
agents/housekeeper/system-prompt/firing-order.json
```

## Main Folder Map

```text
agent-housekeeper/
├── README.md
├── ABOUT.md
├── PRD.md
├── LICENSE
├── repo-manifest.md
├── release-ledger.md
├── agents/
│   └── housekeeper/
│       ├── system-prompt/
│       ├── templates/
│       ├── README.md
│       ├── persona.md
│       ├── founder-operating-style.md
│       ├── meticulous-stewardship.md
│       ├── operating-manual.md
│       ├── knowledge-sources.md
│       ├── validation.md
│       ├── graceful-validation.md
│       ├── repo-transformation-guide.md
│       ├── agent-folder-template.md
│       └── feature-ledger-guide.md
├── docs/
├── examples/
├── features/
│   ├── README.md
│   ├── ledger.md
│   └── tickets/
└── tests/
```

## What The Housekeeper Tracks

- README.md
- ABOUT.md
- PRD.md
- LICENSE
- repo-manifest.md
- release-ledger.md
- docs/
- obsidian/ or wiki notes
- journals
- feature ledgers
- feature tickets
- release notes
- agent rules
- system prompt files
- validation reports
- repo transformation plans

## Reusable Workflow

1. Copy or reference this repo.
2. Add `agents/housekeeper/` to a project.
3. Add root files: README, ABOUT, PRD, repo manifest, release ledger.
4. Add feature ledger and tickets.
5. Add a wiki or Obsidian layer.
6. Add journals.
7. Point the agent to the system prompt folder.
8. Let the agent follow the firing order.

## Related Docs

- [About](ABOUT.md)
- [PRD](PRD.md)
- [Repo Manifest](repo-manifest.md)
- [Release Ledger](release-ledger.md)
- [Housekeeper Agent](agents/housekeeper/README.md)
- [Core System Prompt](agents/housekeeper/system-prompt/00-core-system-prompt.md)
- [Firing Order](agents/housekeeper/system-prompt/01-firing-order.md)
- [Repo Transformation Guide](agents/housekeeper/repo-transformation-guide.md)
