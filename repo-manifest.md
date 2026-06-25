# Repo Manifest

## Purpose

The Repo Manifest tells the Housekeeper what files and folders matter.

## Required Root Files

| File | Purpose | Duty |
| --- | --- | --- |
| README.md | Front door | Keep clear and current |
| ABOUT.md | Project identity | Keep aligned with purpose |
| PRD.md | Product requirements | Keep aligned with scope |
| LICENSE | License | Keep present and visible |
| repo-manifest.md | Repo inventory | Update when structure changes |
| release-ledger.md | Release memory | Update when milestones change |

## Required Folders

| Folder | Purpose | Duty |
| --- | --- | --- |
| agents/housekeeper/ | Main agent standard | Keep complete |
| agents/housekeeper/system-prompt/ | First-read instruction layer | Keep ordered |
| agents/housekeeper/templates/ | Reusable templates | Keep useful |
| docs/ | Guides and documentation | Keep organized |
| examples/ | Example project setups | Keep practical |
| features/ | Feature ledger | Keep current |
| features/tickets/ | Small feature tickets | Keep linked from ledger |
| obsidian/ | Wiki knowledge layer | Keep linked and RAG-ready |
| obsidian/journal/ | Decision and memory history | Keep current after major changes |
| tests/ | Validation notes | Keep visible |

## Housekeeper Rule

When a new important file or folder is added, update this manifest.

Also review new guide files in docs when they are added.

## Design Rule Source

See:

```text
docs/repo-design-rules.md
```
