# Operating Manual

## Purpose

This manual explains how the Housekeeper works inside a repo.

## Sole Write Authority (OR-045)

The Housekeeper is the **only** agent that may edit the repo. Every other agent
meets the housekeeper first and submits a change request. The housekeeper acts
as the write API: intake → triage → dispatch to departments → apply → verify.

Other agents must refuse direct file edits and route requesters here.

Report: [docs/sole-write-authority.md](../../docs/sole-write-authority.md)

## Working Loop

```text
Receive change request (from operator or any other agent)
→ Triage scope
→ Dispatch to in-house departments (draft only)
→ Housekeeper applies edits (sole write authority)
→ Link
→ Track
→ Validate
→ Report pipeline stage
```

## Classification Types

- Concept
- Feature
- Journal
- Template
- Rule
- Release
- Manifest update
- Validation item
- Documentation update

## Folder Rules

Use focused folders:

```text
docs/
examples/
features/
features/tickets/
agents/housekeeper/
tests/
```

## Rule

Prefer small focused Markdown files.

Small files are easier to search, chunk, index, and reuse.
