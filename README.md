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

## Notes
- Do not store secrets in plaintext
- Prefer canonical notes over duplicates
- Prefer durable summaries over raw transcripts
- Use Obsidian wikilinks to keep the graph connected
