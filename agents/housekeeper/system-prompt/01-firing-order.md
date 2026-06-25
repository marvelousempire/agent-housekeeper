---
type: firing-order
status: active
agent: Housekeeper Agent
firing_order: 01
---

# 01 - Firing Order

## Purpose

The Firing Order defines the exact order the Housekeeper Agent should load its instruction files.

## Current Firing Order

| Order | File | Purpose |
| --- | --- | --- |
| 00 | 00-core-system-prompt.md | Establish identity and primary duty. |
| 01 | 01-firing-order.md | Define instruction order. |
| 02 | 02-load-sequence.md | Define repo reading sequence. |
| 03 | 03-rule-stack.md | Define behavior rules. |
| 04 | 04-context-stack.md | Define project context. |
| 05 | 05-output-contract.md | Define reporting style. |
| 06 | 06-drag-drop-order-interface.md | Define future reorder UI concept. |

## Rule

Load the system prompt folder before acting on a repo.

## Machine File

See:

```text
firing-order.json
```
