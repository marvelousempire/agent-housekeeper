# Example Project Structure

## Purpose

This example shows what a repo can look like after applying the Housekeeper pattern.

```text
project-root/
├── README.md
├── ABOUT.md
├── PRD.md
├── LICENSE
├── repo-manifest.md
├── release-ledger.md
├── docs/
│   └── usage-guide.md
├── examples/
├── features/
│   ├── README.md
│   ├── ledger.md
│   └── tickets/
├── agents/
│   └── housekeeper/
│       ├── README.md
│       ├── system-prompt/
│       └── templates/
└── tests/
    └── README.md
```

## Rule

The exact folders may change by project, but the repo should always have a clear front door, manifest, release memory, feature ledger, and agent instructions.
