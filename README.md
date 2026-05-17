# Hermes Obsidian Memory Vault

This vault is the long-term external memory system for Hermes.

## Purpose
- Preserve durable knowledge beyond the active model context window
- Store distilled, reusable knowledge instead of raw chat dumps
- Keep project knowledge, user preferences, procedures, decisions, and references searchable and linked

## Start here
- [[Home]] — human-friendly entry point
- [[index]] — catalog of durable knowledge
- [[Memory Architecture]] — memory model and design principles
- [[log]] — append-only operational history
- [[AGENTS]] — operating contract for how Hermes should use this vault

## Main structure
- `inbox/` — temporary capture and staging
- `sessions/` — session history and episodic memory
- `projects/` — canonical project notes
- `concepts/` — stable ideas and definitions
- `entities/` — people, orgs, tools, systems, products
- `references/` — source notes, summaries, documents, transcripts
- `procedures/` — reusable workflows and playbooks
- `decisions/` — important decisions and rationale
- `analyses/` — syntheses, comparisons, and question-driven writeups
- `raw/` — immutable source material and attachments
- `templates/` — reusable note templates

## How Hermes uses this vault
1. Capture incoming information
2. Classify it by memory type
3. Distill the durable signal
4. Update an existing canonical note when possible
5. Create a new note only when needed
6. Add wikilinks to related notes
7. Update indexes when a durable note is added
8. Append important maintenance actions to [[log]]

## Management policy
This vault currently uses a hybrid management model:
- Hermes may autonomously maintain routine notes, links, indexes, and memory hygiene
- Hermes should ask before major restructures, bulk renames, bulk deletions, or schema changes

See also:
- [[Vault Management Policy]]
- [[Memory Ingestion Workflow]]

## Vault activation prompts
Use these ready-made prompts when you want Hermes to adopt this vault as the active external memory system.

### Normal activation prompt
Use when starting a new session or when you want standard vault-backed work without a full audit.

```text
Use the current folder’s Obsidian vault as canonical external memory. Read the root docs first and follow the documented hybrid memory-management workflow for this session.
```

### Deeper index-loading prompt
Use when you want broader context before starting work, but not a full vault-wide audit.

```text
Use the current folder’s Obsidian vault as canonical external memory. Read the root docs and all major index notes before continuing, then use the documented hybrid memory workflow for this session.
```

### Full vault audit prompt
Use after a long gap, before cleanup, after major changes, or when you want Hermes to refresh its understanding of the whole vault.

```text
Use the current folder’s Obsidian vault as canonical external memory. Audit the whole vault, refresh your map of the existing notes and structure, then continue using the documented hybrid memory workflow.
```

Recommendation:
- default to the normal activation prompt
- use the deeper index-loading prompt when you want more context up front
- use the full vault audit prompt only when broader reorientation is actually useful

See also:
- [[Vault Activation Prompts]]

## Notes
- Do not store secrets in plaintext
- Prefer canonical notes over duplicates
- Prefer durable summaries over raw transcripts
- Use Obsidian wikilinks to keep the graph connected
