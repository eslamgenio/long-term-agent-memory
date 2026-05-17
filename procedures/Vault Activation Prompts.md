# Vault Activation Prompts

## Purpose
Ready-made prompts for telling Hermes to adopt this Obsidian vault as the active external memory system.

## 1. Normal activation prompt
Use when starting a new session or when you want standard vault-backed work without a full audit.

```text
Use the current folder’s Obsidian vault as canonical external memory. Read the root docs first and follow the documented hybrid memory-management workflow for this session.
```

What it implies:
- read root control notes
- adopt the documented policy and note taxonomy
- do targeted retrieval from relevant notes
- update the vault incrementally during the task

## 2. Deeper index-loading prompt
Use when you want broader context before starting work, but not a full vault-wide audit.

```text
Use the current folder’s Obsidian vault as canonical external memory. Read the root docs and all major index notes before continuing, then use the documented hybrid memory workflow for this session.
```

What it implies:
- read root control notes
- read index notes such as `[[Projects Index]]`, `[[Concepts Index]]`, `[[Procedures Index]]`, `[[Decisions Index]]`, `[[Sessions Index]]`, and `[[References Index]]`
- build a broader map of the vault before continuing
- update memory incrementally during the task

## 3. Full vault audit prompt
Use after a long gap, before cleanup, after major changes, or when you want Hermes to refresh its understanding of the whole vault.

```text
Use the current folder’s Obsidian vault as canonical external memory. Audit the whole vault, refresh your map of the existing notes and structure, then continue using the documented hybrid memory workflow.
```

What it implies:
- read root control notes
- inspect the vault structure more broadly
- refresh understanding of existing notes, folders, and navigation
- identify missing links, duplicates, or stale areas if relevant
- continue with the task after the audit

## Recommendation
Default to the normal activation prompt.
Use the deeper index-loading prompt when you want more context up front.
Use the full vault audit prompt only when broader reorientation is actually useful.

## Related Pages
- [[README]]
- [[Home]]
- [[Memory Architecture]]
- [[Vault Management Policy]]
- [[Memory Ingestion Workflow]]
