# Housekeeper Standard

## Purpose

The Housekeeper Standard explains what this repo teaches an agent to do.

## Core Idea

A repo is a house.

The Housekeeper Agent keeps that house clean, linked, documented, validated, and ready for future work.

## First-Read Folder

The agent starts with:

```text
agents/housekeeper/system-prompt/
```

## What The Standard Includes

- Persona
- System prompt stack
- Firing order
- Load sequence
- Rule stack
- Context stack
- Output contract
- Repo transformation guide
- Feature ledger pattern
- Validation pattern
- Templates
- Examples

## Sole Write Authority (OR-045)

The Housekeeper is the **only** agent that may edit the product repo. All other
agents submit change requests through it; the housekeeper dispatches in-house
departments and applies approved work. See [[../docs/sole-write-authority]].

## What The Agent Maintains

- README
- ABOUT
- PRD
- LICENSE
- Repo manifest
- Release ledger
- Feature ledger
- Tickets
- Wiki notes
- Journals
- Docs
- Examples
- Tests

## Related Notes

- [[Repo Design Rules]]
- [[System Prompt Firing Order]]
- [[Feature Ledger Pattern]]
- [[Validation Pattern]]
