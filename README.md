# Agent Housekeeper

**Keep the house clean. Keep the memory clear. Keep the repo ready.**

Agent Housekeeper is a reusable repo-management agent standard.

It defines how an AI agent should act as a project housekeeper: reading the repo, preserving founder intent, organizing docs, maintaining README files, tracking features, creating journals, keeping release memory, validating changes, and preparing the repo for RAG, Obsidian, and AI-assisted workflows.

This is not only a clever tagline. The repo backs it up with a working system prompt stack, firing order, validation process, feature ledger, repo manifest, release ledger, wiki layer, journal layer, and reusable workflow.

## Purpose

This repo is the reusable standard for Housekeeper Agents.

A project can point an agent to this repo so the agent understands how to set up and maintain a clean, modular, wiki-ready, RAG-ready project structure.

## Schema Alignment

Agent Housekeeper follows the schema family:

```text
schema-agent   = how this agent standard is built
schema-gitrepo = how this repo is structured
```

Agent Housekeeper is the first working reusable agent standard built from this style.

## Core Idea

A repo is a house.

The Housekeeper Agent keeps the house organized. It knows which files matter,
which folders must exist, which ledgers must be updated, and which rules should
fire first.

## Sole Write Authority (OR-045)

The Housekeeper is the **only** agent that may edit a product repo. Every other
agent submits change requests through it — the housekeeper acts as the write
API, dispatches in-house departments, and applies approved edits itself. No
rogue AI writes around the gatekeeper.

Report: [docs/sole-write-authority.md](docs/sole-write-authority.md)

## Shared Source Skill

When the same reusable standard is needed by more than one repo, the Housekeeper should help keep one main standard and let other repos reference it.

This reduces duplicate maintenance and keeps the standard easier to improve.

Read:

- [Shared Source Management](docs/shared-source-management.md)
- [Submodule Management Principle](docs/submodule-management-principle.md)

## Proof In The Repo

The Housekeeper idea is backed by actual project structure:

```text
agents/housekeeper/system-prompt/
agents/housekeeper/system-prompt/firing-order.json
agents/housekeeper/persona.md
agents/housekeeper/knowledge-sources.md
agents/housekeeper/repo-transformation-guide.md
agents/housekeeper/validation.md
features/ledger.md
obsidian/
obsidian/journal/
repo-manifest.md
release-ledger.md
```

The repo says where the agent should start, what order it should follow, which files matter, how features are tracked, how decisions are remembered, and how work is validated.

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

## Motif Design Alignment

This repo follows the Motif-style repo design rules.

Read:

- [Repo Design Rules](docs/repo-design-rules.md)
- [Motif Design Alignment Audit](docs/motif-design-alignment-audit.md)
- [Agent Housekeeper Wiki](obsidian/README.md)

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
├── docs/
├── examples/
├── features/
├── obsidian/
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
- obsidian/
- obsidian/journal/
- feature ledgers
- feature tickets
- release notes
- agent rules
- system prompt files
- validation reports
- repo transformation plans
- shared source plans

## Feature Ledger

- [Feature Ledger README](features/README.md)
- [Feature Ledger](features/ledger.md)

## Wiki Layer

- [Agent Housekeeper Wiki](obsidian/README.md)
- [Housekeeper Standard](obsidian/Housekeeper%20Standard.md)
- [Repo Design Rules](obsidian/Repo%20Design%20Rules.md)
- [System Prompt Firing Order](obsidian/System%20Prompt%20Firing%20Order.md)
- [Feature Ledger Pattern](obsidian/Feature%20Ledger%20Pattern.md)
- [Validation Pattern](obsidian/Validation%20Pattern.md)

## Journal

- [Journal Update - Motif Design Alignment](obsidian/journal/Journal%20Update%20-%20Motif%20Design%20Alignment.md)

## Reusable Workflow

1. Copy or reference this repo.
2. Add `agents/housekeeper/` to a project.
3. Add root files: README, ABOUT, PRD, repo manifest, release ledger.
4. Add feature ledger and tickets.
5. Add a wiki or Obsidian layer.
6. Add journals.
7. Point the agent to the system prompt folder.
8. Let the agent follow the firing order.
9. When a copied reusable standard gets hard to manage, create a shared source plan.

## Related Docs

- [About](ABOUT.md)
- [PRD](PRD.md)
- [Repo Manifest](repo-manifest.md)
- [Release Ledger](release-ledger.md)
- [Housekeeper Agent](agents/housekeeper/README.md)
- [Core System Prompt](agents/housekeeper/system-prompt/00-core-system-prompt.md)
- [Firing Order](agents/housekeeper/system-prompt/01-firing-order.md)
- [Repo Transformation Guide](agents/housekeeper/repo-transformation-guide.md)
- [Shared Source Management](docs/shared-source-management.md)
- [Submodule Management Principle](docs/submodule-management-principle.md)
