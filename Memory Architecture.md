# Memory Architecture

## Goal
Extend an AI agent with a filesystem-based persistent memory system that survives beyond the model context window.

## Design principles
- Distill, do not dump.
- Prefer canonical notes over duplicates.
- Separate temporary, episodic, semantic, and procedural memory.
- Link related notes aggressively with wikilinks.
- Preserve provenance for source-backed claims.
- Periodically merge, prune, and re-index.

## Memory layers
### Working memory
- Location: `inbox/`
- Purpose: temporary capture and staging
- Retention: short-lived unless promoted

### Episodic memory
- Location: `sessions/`
- Purpose: preserve session history, decisions, outcomes, and follow-ups
- Retention: medium to long

### Semantic memory
- Location: `projects/`, `concepts/`, `entities/`, `references/`
- Purpose: durable facts and structured knowledge
- Retention: long-term

### Procedural memory
- Location: `procedures/`
- Purpose: reusable workflows and playbooks
- Retention: long-term, periodically revised

### Decision memory
- Location: `decisions/`
- Purpose: capture major choices and rationale
- Retention: long-term

## Promotion pipeline
1. Capture notes in `inbox/` or `sessions/`.
2. Extract durable facts, procedures, and decisions.
3. Update existing canonical notes first.
4. Create new notes only when the concept is stable and reusable.
5. Add links from index notes and related notes.
6. Record meaningful maintenance actions in `[[log]]`.

## Retrieval strategy
- Start from `[[Home]]` or `[[index]]`.
- Use index notes as maps of content.
- Follow wikilinks between concept, project, procedure, and decision notes.
- Prefer durable notes over re-reading old sessions when possible.

## Maintenance strategy
- Merge duplicate notes.
- Archive or delete stale scratch notes.
- Mark outdated procedures explicitly.
- Re-verify environment-specific facts.
- Expand indexes as the vault grows.
