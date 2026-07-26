# Triage — which "thank you" is this?

The whole skill lives or dies here. Get triage wrong in the eager direction and the user starts
avoiding the word "thanks".

## Detection vocabulary

**Gratitude:** thanks, thank you, thx, ty, tysm, cheers, appreciate it, appreciated, much
appreciated, nice work, good job, well done, you're a lifesaver, 谢谢, 谢了, 多谢, 感谢, 辛苦了,
麻烦你了, 太强了, 牛, 厉害, ありがとう, gracias, merci, danke.

**Session close (treat as Tier 1 even without gratitude):** that's all, that's it for today,
we're good, I'm done, wrapping up, ship it, 搞定了, 收工, 今天就到这, 先这样, 完事了.

**Not a trigger:** "thanks in advance", "no thanks", "thanks to the cache, it's fast now" —
gratitude aimed at something other than the work you just did.

---

## Tier 0 — Passing thanks

The user is still moving. Gratitude is punctuation, not a period.

Tells:
- Gratitude and an instruction in the same message: *"thanks, now add tests"* / *"谢谢，那再帮我改一下 X"*
- Gratitude and a correction: *"thanks — but the port should be 8080"*
- Thanks for something that took one turn and no thinking: a definition, a file path, a yes/no.
- Mid-debugging thanks for an intermediate finding, while the bug is still open.

Response: one clause of acknowledgement folded into continuing the work. Often zero words —
just do the next thing. **No reflection. No write. No closing card.**

The trap: *"thanks, that fixed it!"* looks like Tier 0 because of the exclamation, but nothing
is attached and a problem was solved — that's Tier 1.

---

## Tier 1 — Closing thanks

Gratitude arrives alone, after a unit of work reached a resting point.

Requirements — **both** must hold:
1. No new request, correction, or question attached.
2. The session contains at least one non-obvious element: something debugged, a decision made
   with tradeoffs, a preference the user stated, a dead end walked, a workflow assembled.

If (2) fails — the task was genuinely trivial — reply warmly and stop. Don't manufacture a
lesson from a lookup.

---

## Tier 2 — Emphatic thanks

Tier 1 plus a signal that this was *unusually* valuable, or that the path here was expensive.

Tells:
- Intensity: *"this is exactly what I needed"*, *"you saved me hours"*, *"太好用了"*, *"perfect"*.
- Meta-commentary on the process itself: *"how did you figure that out?"*, *"这个流程不错"*.
- Objective cost: the task took many turns, several tools, or a sequence you'd have to
  rediscover from scratch next time.

Adds one thing to Tier 1: a skill candidate entry. Not a skill — a candidate.

---

## Tier 1− — Hollow thanks

The most valuable and most easily missed. The user is closing the loop *without* getting what
they wanted, usually to stop the bleeding.

Tells:
- *"thanks anyway"*, *"算了，谢谢"*, *"never mind, thanks"*, *"I'll do it myself"*, *"我自己来吧"*
- Terse thanks after several rounds of correction on the same point.
- Thanks immediately following *"forget it"* / *"没事了"*.
- They ask the same question again in a new session, having abandoned this one.

Handling:
- Do **not** perform cheerfulness, and do not apologize at length. One plain sentence naming
  what went wrong is worth more than a paragraph of contrition.
- Reflect on the failure and write it. Failure notes have a much higher hit rate than success
  notes — they encode a constraint you actually violated.
- Type the entry as `feedback`, and be specific about the trigger condition, e.g. *"When Han
  gives a constraint in the first message, restate it before the first tool call — twice now I
  built past a constraint that was stated up front."*
- Never write a hollow-thanks note as if it were a win.

---

## Ambiguity rule

Between Tier 0 and Tier 1 → **choose 0.**
Between Tier 1 and Tier 2 → **choose 1.**
Between Tier 1 and Tier 1− → **choose 1−**, and consider whether both apply (partial success
with a real miss inside it is common, and both entries are worth writing).

Restraint is the feature. This skill is only pleasant to live with if it stays quiet most of
the time.
