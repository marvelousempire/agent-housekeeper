---
type: interface-concept
status: active
agent: Housekeeper Agent
firing_order: 06
---

# 06 - Drag Drop Order Interface

## Purpose

This note describes a future visual interface for changing the firing order.

## Concept

The user sees rule files as cards.

The user drags the cards into the desired order.

The saved order updates the machine-readable firing order.

## Files To Update

```text
agents/housekeeper/system-prompt/firing-order.json
agents/housekeeper/system-prompt/01-firing-order.md
```

## Future Interface Options

- HTML page
- Local web app
- WordPress admin page
- Obsidian plugin view
- GitHub Pages tool
- JSON editor

## Protected Rule

The core system prompt should stay first unless advanced mode is enabled.
