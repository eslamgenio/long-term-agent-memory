# Memory Ingestion Workflow

## Purpose
Define the end-to-end process an AI agent follows to turn new information into durable, retrievable memory inside this vault.

## When to use
Use this workflow whenever new information arrives through conversation, files, links, documents, transcripts, project work, or source ingestion.

## Core principle
Do not dump raw interaction history into the vault. Capture first, then distill, promote, link, index, and log.

## End-to-end flow

### 1. Observe incoming information
Identify the new material:
- a user preference
- a project fact
- a concept or definition
- a workflow or procedure
- a decision and rationale
- a document, URL, or transcript
- a session outcome

### 2. Classify the information
Decide which memory type applies.

- Working memory -> `inbox/`
- Episodic memory -> `sessions/`
- Semantic memory -> `projects/`, `concepts/`, `entities/`, `references/`
- Procedural memory -> `procedures/`
- Decision memory -> `decisions/`
- Synthesized conclusions -> `analyses/`

### 3. Capture without overcommitting
If the material is incomplete, noisy, or still under exploration, capture it temporarily first.

Preferred locations:
- `inbox/` for scratch capture and staging
- `sessions/` for session-level history and context
- `raw/` for immutable original source files

### 4. Distill the durable signal
Extract only what is worth keeping long-term.

Keep:
- durable facts
- stable preferences
- reusable procedures
- important decisions
- source-backed summaries
- reusable project knowledge

Avoid storing as primary memory:
- raw chat dumps
- verbose intermediate reasoning
- repeated discussion with no durable conclusion
- ephemeral task state
- secrets in plaintext

### 5. Check for an existing canonical note
Before creating a new note, search for an existing note that should be updated.

Rules:
- prefer updating one canonical note over creating duplicates
- create a new note only when the concept is genuinely distinct and reusable
- if two notes overlap strongly, prefer consolidation later

### 6. Write to the correct durable note type
Typical destinations:
- user/project preference -> existing profile or project note
- stable project knowledge -> `projects/`
- reusable concept -> `concepts/`
- person/org/tool/system -> `entities/`
- source summary -> `references/`
- repeatable workflow -> `procedures/`
- important choice -> `decisions/`
- synthesis or answer with evidence -> `analyses/`
- session history -> `sessions/`

### 7. Preserve provenance when relevant
For source-backed claims, record where the information came from.

Examples:
- source file path in `raw/`
- URL or document title
- date retrieved or discussed
- confidence or uncertainty notes

### 8. Link the note into the graph
Add wikilinks to related notes so the vault remains navigable.

Common targets:
- `[[Home]]`
- `[[index]]`
- relevant index notes
- related project, concept, procedure, decision, reference, or session notes

Goal:
- improve backlinks
- improve graph quality
- make retrieval easier in future sessions

### 9. Update navigation notes
If the new note is durable and important, update the relevant index notes.

Usually one or more of:
- `[[Projects Index]]`
- `[[Concepts Index]]`
- `[[Procedures Index]]`
- `[[Decisions Index]]`
- `[[Sessions Index]]`
- `[[References Index]]`
- `[[index]]`

### 10. Append to the operational log
If the action materially changes the vault, append a concise entry to `[[log]]`.

Examples:
- created a new procedure note
- ingested a source
- created a decision note
- merged duplicate notes
- updated the vault policy

### 11. Retrieve canonically later
On future tasks:
1. start from `[[Home]]` or `[[index]]`
2. follow the relevant index note
3. read canonical durable notes first
4. use session notes only for historical context when needed

### 12. Maintain memory quality over time
Periodically:
- merge duplicates
- relink orphan notes
- archive or delete stale scratch notes
- mark outdated procedures
- re-verify environment-specific facts
- refine note titles when needed

## Practical examples

### Example A: user preference
Input:
- user says they prefer concise responses

Flow:
1. classify as durable preference
2. update `[[User Profile]]`
3. link if helpful
4. log only if the change is meaningful to vault policy or long-term behavior

### Example B: new source document
Input:
- user provides a PDF or URL

Flow:
1. store original in `raw/` when appropriate
2. create or update a note in `references/`
3. extract concepts, entities, and decisions
4. update canonical notes instead of duplicating facts
5. link related notes
6. update indexes
7. append a log entry

### Example C: reusable workflow discovered during work
Input:
- repeated debugging or deployment steps recur across sessions

Flow:
1. classify as procedural memory
2. create or update a note in `procedures/`
3. link to the project or concept it supports
4. update `[[Procedures Index]]`
5. log the addition if it materially improves the vault

## Hybrid-policy reminder
Under the current policy, the agent may autonomously perform routine ingestion and maintenance. The agent should ask first before:
- major restructures
- bulk renames
- bulk deletions
- schema changes
- high-impact reinterpretation of user-authored content

## Related Pages
- [[Memory Architecture]]
- [[Vault Management Policy]]
- [[User Profile]]
- [[index]]
- [[log]]
