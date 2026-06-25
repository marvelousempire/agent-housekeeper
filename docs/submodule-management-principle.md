# Submodule Management Principle

## Purpose

This file teaches the Housekeeper Agent when and how to use a Git submodule strategy.

A submodule is useful when one repo should follow another repo as a reusable source standard without copying the same files forever.

## Core Principle

Do not duplicate a reusable standard across multiple repos when one repo can become the source standard.

Use a submodule when the same folder, rule set, template system, agent standard, or shared library needs to be reused across projects while staying connected to its original source.

## Why This Matters

Duplication creates drift.

If the same Housekeeper files live in two repos, one version may change while the other stays old.

A submodule lets one repo point to the reusable standard instead of manually copying it.

## When To Use A Submodule

Use a submodule when:

- A reusable standard has its own repo.
- Multiple projects should follow the same standard.
- The shared folder should keep its own history.
- The project should pin a known version of the standard.
- Updates should be deliberate instead of automatic.
- Copying the same folder would create maintenance drift.

## Good Submodule Examples

- Reusable agent standards
- Shared prompt systems
- Shared templates
- Shared design systems
- Shared documentation standards
- Shared plugin modules
- Shared SDKs
- Shared test suites

## When Not To Use A Submodule

Do not use a submodule when:

- The folder is small and project-specific.
- The files will never be reused elsewhere.
- The project needs frequent direct edits inside the folder.
- The team does not want to manage submodule updates.
- A normal package manager would be cleaner.

## Preferred Layout

```text
project-repo/
├── vendor/
│   └── shared-standard/       # submodule source
└── local-folder/
    └── project-overrides/     # local project notes and overrides
```

## Housekeeper Pattern

For Housekeeper standards, use:

```text
project-repo/
├── vendor/
│   └── agent-housekeeper/     # reusable standard submodule
└── agents/
    └── housekeeper/           # local pointer and project-specific overrides
```

## Local Folder Rule

The local project folder should not keep a full duplicate of the reusable standard.

It should keep only:

- Source manifest
- Local override notes
- Project-specific context
- Project-specific links
- Migration notes

## Required Documentation Updates

When a submodule is added, the Housekeeper should update:

- `.gitmodules`
- README.md
- repo-manifest.md
- release-ledger.md
- feature ledger
- source manifest
- docs explaining the submodule strategy
- journal entry when project memory changes

## Safe Migration Steps

1. Identify duplicated standard files.
2. Confirm the reusable standard repo exists.
3. Add `.gitmodules` or use `git submodule add`.
4. Add the submodule path under `vendor/` or another clear external-source folder.
5. Update README and repo-manifest.
6. Update release-ledger.
7. Add a feature ticket for the migration.
8. Keep the local duplicate temporarily.
9. Confirm the submodule works in a normal Git client.
10. Prune local duplicated files.
11. Keep a lightweight local pointer and override layer.

## Git Commands

Add a submodule:

```bash
git submodule add -b main https://github.com/OWNER/REPO.git vendor/REPO
```

Initialize submodules after clone:

```bash
git submodule update --init --recursive
```

Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/OWNER/PROJECT.git
```

Update a submodule to the latest remote commit:

```bash
cd vendor/REPO
git fetch
git checkout main
git pull
cd ../..
git add vendor/REPO
git commit -m "Update REPO submodule"
```

## Validation Checklist

- `.gitmodules` exists.
- Submodule path exists.
- README explains the submodule.
- repo-manifest lists the submodule.
- release-ledger records the milestone.
- Local duplicate files are pruned or marked temporary.
- Local folder explains it is a pointer or override layer.

## Related Files

- docs/repo-design-rules.md
- agents/housekeeper/meticulous-stewardship.md
- agents/housekeeper/system-prompt/03-rule-stack.md
- features/ledger.md
