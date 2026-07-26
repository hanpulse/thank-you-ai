---
name: thank-you-ai
description: "Turn a genuine thank-you or explicit session close into a brief closing ritual: distinguish passing politeness from a completed unit of work, capture only the lesson that would change a future agent’s first move, and record repeatable workflows as skill candidates. Use for standalone thanks, thank you, thx, appreciate it, 谢谢, 谢了, 多谢, 感谢, 辛苦了, 太强了, 搞定了, 收工, or done for today. Do not use when gratitude accompanies a new request, correction, or question."
---

# Thank You, AI

Treat a genuine closing thank-you as a low-friction chance to close the loop and retain one useful lesson. Write only what would change a cold agent's first move on a future task. A zero-entry reflection is valid.

## Resolve the host before writing

Before any write, read the host, project, and user-provided instructions. Their memory location, write authority, privacy rules, and append-only rules override this skill. Follow references/storage.md to select one store. Do not create a competing memory system when one already exists.

## Workflow

### 1. Detect and triage

Choose exactly one tier:

| Tier | Condition | Action |
| --- | --- | --- |
| 0 · Passing | Gratitude includes a new request, correction, question, or follows a trivial lookup | Acknowledge briefly and continue. Do not reflect or write. |
| 1 · Closing | Standalone closing thanks after a non-obvious decision, discovery, preference, or completed piece of work | Reflect, capture any keeper, then close. |
| 2 · Emphatic | Tier 1 plus unusually high value or a costly, repeatable process | Tier 1 plus one skill-candidate record. |
| 1− · Hollow | “Thanks anyway,” “never mind,” “算了，谢谢,” or the user gives up after failed work | Capture the failure precisely, then close without cheerfulness. |

When uncertain between 0 and 1, choose 0. When uncertain between 1 and 2, choose 1. Read references/triage.md for examples.

### 2. Reflect silently

Keep only a lesson that passes the rewind test: would it change the first five minutes of the next attempt? Consider the shortcut, a plausible dead end, an explicit user preference, an undocumented environment fact, or a repeatable process. For hollow thanks, name the missed constraint or wrong assumption plainly. Read references/reflection.md when needed.

### 3. Capture with restraint

Search the selected store first. Follow its update and ownership rules; if it is append-only, append a correction or new entry rather than rewriting another agent's work. Record one fact per entry, with an absolute date and enough context to apply it. Never store secrets, credentials, private personal information, or task-state that belongs in a tracker.

For Tier 2, record a candidate only. Promote it to a real skill only after a second sighting, explicit user approval, or a proven costly multi-step process—and ask before promotion.

### 4. Close

Reply in the user's language in two to four warm, factual lines:

    Done: <what finished>
    Learned: <one useful lesson> → saved to <path>, or “nothing new worth saving”
    Skill candidate: <name> (seen 2×) — worth formalizing?  [Tier 2 only]

Then stop. Do not manufacture gratitude, add unsolicited next steps, flatter the user, or summarize the whole transcript.

## References

- references/triage.md — tier examples and edge cases.
- references/reflection.md — rewind test, failure analysis, and entry quality.
- references/storage.md — portable memory-store resolution and safety rules.
