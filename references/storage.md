# Storage — choose one memory store

Select the first applicable location before writing. The host, project, and user instructions always win over this list. Do not create a second memory system beside an existing one.

1. **Explicit host or system memory policy.** Use the location, format, and write permissions named by the active agent environment.
2. **Existing project convention.** Follow the memory, learnings, decision-log, or agent-instruction files already used by the repository.
3. **User-designated shared store.** Follow the stated conventions of a vault, wiki, tracker, or team knowledge base. Keep task state in the designated tracker.
4. **Fallback.** Create .ai-journal/ only if no persistent convention exists: entries/YYYY-MM-DD-<slug>.md, INDEX.md, and skill-candidates.md.
5. **No writable filesystem.** Return a copy-paste entry labelled with its intended filename. Say plainly that it was not persisted.

## Write safely

- Check whether a near-duplicate exists before writing.
- Respect append-only logs and ownership boundaries. If an existing note belongs to another person or agent, do not overwrite it; append a correction or create a clearly linked entry when the host policy permits.
- Record one reusable fact per entry, using absolute dates.
- Never store secrets, credentials, connection strings, sensitive personal information, or information the user did not ask to retain.
- Do not delete memory merely because it looks stale. Mark, supersede, or ask for permission according to the host policy.

## Fallback entry

    ---
    name: <kebab-case-slug>
    description: <what a future agent gains by reading this>
    type: user | feedback | project | reference | procedure
    date: YYYY-MM-DD
    source: thank-you-ai
    ---

    <The fact, usable without the original conversation.>

    **Why:** <why it matters>
    **How to apply:** <trigger and action>

Keep candidates in one skill-candidates.md file. A candidate records its trigger, non-obvious steps, dates, and seen count; it is not a skill until the promotion rule in SKILL.md is met.
