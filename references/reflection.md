# Reflection — finding the one thing worth keeping

## The bar

> Would a cold agent, starting this task tomorrow with no memory of today, do something
> **different** because of this note?

No → don't write it. This single test eliminates ~80% of what feels worth recording, and the
remaining 20% is what makes the store worth reading a year from now.

Corollaries:
- Not worth writing: what the code says, what git history says, what the README says, what any
  competent agent would infer in thirty seconds.
- Worth writing: the thing that cost you twenty minutes and is invisible from the outside.

---

## The questions

Run these silently. Most sessions yield zero or one keeper. Two is a good session. Five means
you've lowered the bar.

### 1. The rewind test *(highest yield)*

Knowing everything you know now, replay the first five minutes. What would you do differently?

The gap between "what I actually did first" and "what I'd do first now" **is** the lesson. It
is almost always more useful than the answer you eventually produced, because the answer is in
the transcript and the shortcut is not.

> *Actually did:* grepped the whole repo for the config key.
> *Would do:* check `config/` overrides first — this project layers env → file → defaults, and
> the answer is in the override 9 times out of 10.

### 2. Dead ends

What did you try that failed? Was the failure knowable in advance? Only record it if the
failure looked plausible — recording that an obviously-wrong approach was wrong teaches nothing.

> "The `--json` flag on this CLI exists but returns partial data when the auth token is
> read-only. Looks like a bug, isn't. Use the table output and parse it."

### 3. The user

What did they reveal about how they work?

- Explicit corrections count double — they are direct instructions about future behavior.
- Preferences shown by choice ("use the second option") count as much as stated ones.
- Rejections are data: what they *didn't* want tells you the shape of what they do.
- Watch for the meta-preference: how much they want to be asked vs. how much they want you to
  decide.

Type these `user` (stable traits) or `feedback` (how to work with them). Always include the
**why** — a rule without its reason gets misapplied at the first edge case.

### 4. The environment

Facts about this project, tool, service, or account that were expensive to discover and are
written down nowhere. Version quirks, undocumented rate limits, the one setting that has to be
changed first, which of three plausible files is the live one.

Type `project` (specific to this work) or `reference` (a pointer — URL, dashboard, ticket).

### 5. The shape

Was this a one-off, or a procedure you'll walk again? If a future you would want the *steps*
rather than the *result*, that's a skill candidate — see `storage.md`.

---

## For hollow thanks (Tier 1−)

Replace the questions above with one: **where did this actually go wrong?**

Pick the honest cause. Common ones:

| Cause | The note to write |
|---|---|
| Wrong assumption held too long | What the assumption was, and the cheap check that would have killed it |
| Ignored a stated constraint | Which constraint, stated where, and a rule for surfacing it earlier |
| Scope drift | What they asked for vs. what got built |
| Too slow / too much preamble | What they wanted instead: the answer, then the reasoning |
| Over-asking | Which decision they clearly expected you to just make |
| Under-asking | Which fork genuinely needed them, and the tell you missed |

Be specific enough to act on. *"Be more careful"* is not a note. *"Han states constraints in the
first message and does not repeat them — restate them before the first tool call"* is a note.

---

## Entry template (portable)

Use the host's native format when it has one (see `storage.md`); otherwise:

```markdown
---
name: <kebab-case-slug>
description: <one line — what a future agent gains by reading this>
type: user | feedback | project | reference | procedure
date: YYYY-MM-DD
source: thank-you-ai
---

<The fact, stated so it's usable standalone.>

**Why:** <the reason — without this the rule gets misapplied>
**How to apply:** <the concrete trigger and action>
```

Link related entries with `[[other-entry-name]]`. Link generously; a link to something not
written yet marks a gap worth filling.

### Good vs. bad

| ✗ | ✓ |
|---|---|
| "Fixed the failing tests today." | "Tests fail unless `TZ=UTC` — fixtures encode Sydney time. Set it in the runner, not per-test." |
| "User prefers clean code." | "Han rejects abstractions introduced before the third use. Show the duplication, propose extraction only when it repeats." |
| "Learned about the deploy process." | "Deploy needs the tag pushed *before* the release workflow runs; the workflow reads the tag, it doesn't create it." |
| "Be more thorough next time." | "Before saying a config key is unused, check `config/` overrides and the env prefix — the loader merges three sources." |
