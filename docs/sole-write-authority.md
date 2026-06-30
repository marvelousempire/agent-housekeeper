# Sole Write Authority — Housekeeper as the Only Repo Editor

**Status:** locked standard (OR-045)  
**Audience:** every agent, operator assistant, and department agent working on a product repo

## One sentence

The **Housekeeper Agent** is the **only** agent that may edit a product's git tree. Every other agent submits change requests through the housekeeper, which acts as the **write API** — intake, triage, dispatch, apply, verify.

## Why

Fleet agents (Cursor, Claude, Grok, Hermes, reviewers, builders, snitches) can read and draft freely, but only one scoped authority applies edits. That prevents rogue AI from corrupting real code, drifting CHANGELOGs, or bypassing verify gates.

## Roles

| Role | May do | May NOT do |
|------|--------|------------|
| **Housekeeper** (one per product repo) | Accept change requests · plan work · dispatch to in-house departments · apply approved edits · run verify gates · report pipeline stage | Guess outside bounded corpus · skip verify · let other agents write around it |
| **Any other agent** | Read corpus · research · draft plans · file handoffs · **submit instructions to the housekeeper** | `git commit`, file writes, mutating `make` targets, or any repo edit without housekeeper dispatch |
| **Operator (human)** | Boss Moves · approve/reject housekeeper plans · emergency override | Routine product edits that bypass the housekeeper |

## Request flow

```text
Operator / Cursor / Claude / Grok / Hermes / department agent
        │
        │  change request (what, why, files, verify gate)
        ▼
   Housekeeper Agent  ◄── sole write API for this repo
        │
        ├── dispatch → builder / docs / deploy / audit departments
        ├── apply    → only housekeeper performs file edits + commits
        └── verify   → pass/fail → report pipeline stage with proof
```

## In practice

1. **Meet the housekeeper** — load this repo's housekeeper context before asking for any repo change.
2. **Submit a change request** — what to change, why, which files, which verify gate proves done.
3. **Housekeeper triages** — accepts, rejects, or routes to the correct product housekeeper if out of scope.
4. **Housekeeper dispatches** — breaks work into department tasks. Departments **draft and advise**; they do not write to git alone.
5. **Housekeeper applies** — only the housekeeper session (or operator acting through it) edits files, commits, and runs verify.
6. **Housekeeper reports** — names pipeline stage: committed → pushed → PR → merged → deployed → live.

## Refusal rule (non-negotiable)

If any agent is asked to edit files and is **not** the housekeeper for that repo, it must stop and say:

```text
Change requests go through the housekeeper for <repo-id>.
I can draft a plan or handoff, but I will not write to the repo directly.
```

## Related

- [Operating Manual](../agents/housekeeper/operating-manual.md)
- [Rule Stack](../agents/housekeeper/system-prompt/03-rule-stack.md)
- [Core System Prompt](../agents/housekeeper/system-prompt/00-core-system-prompt.md)
- Nephew canon: `docs/pockit/Housekeeper-Architecture.md` § sole write authority