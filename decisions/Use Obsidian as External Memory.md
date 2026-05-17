# Use Obsidian as External Memory

## Status
Accepted

## Decision
Use the current folder as an Obsidian vault dedicated to AI-agent external persistent memory.

## Rationale
- The model context window is limited.
- Durable knowledge should survive across sessions.
- Markdown files are transparent, portable, searchable, and easy to maintain.
- Obsidian adds linking, graph navigation, templates, search, and structured organization.

## Consequences
- Knowledge must be curated rather than dumped.
- The vault will maintain canonical notes and index notes.
- Session history and durable knowledge will be stored separately.
- Ongoing maintenance is required to prevent duplication and drift.

## Related Pages
- [[Memory Architecture]]
- [[Home]]
- [[User Profile]]
