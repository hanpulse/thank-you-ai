# Thank You, AI

<p align="center">
  <img src="./assets/readme/hero.svg" width="100%" alt="Thank You, AI — a closing ritual for agent conversations. Triage: 0 Passing, 1 Closing, 2 Emphatic, 1− Hollow.">
</p>

An Agent Skills skill that turns a genuine end-of-task “thank you” into a quiet closing ritual: retain one high-value lesson, not a diary entry.

## Install

Copy the entire thank-you-ai directory—including references—into the skills directory your agent host uses.

    Claude Code: ~/.claude/skills/thank-you-ai/
    Codex:       ~/.codex/skills/thank-you-ai/

It also works as a project-local skill when placed in that host's supported project skill directory.

## Behaviour

The skill deliberately ignores polite “thanks” that contain another instruction. For a genuine close, it uses four tiers: passing, closing, emphatic, and hollow/failed. It writes only a lesson that would change the next agent's first move, and asks before turning a repeated procedure into a new skill.

The current host's instructions always decide where, whether, and how persistent memory may be written. The fallback journal is used only when no host or project convention exists.

## Portability

SKILL.md follows the Agent Skills convention and has no vendor-specific tools or paths. Codex-specific UI metadata lives in agents/openai.yaml; hosts that do not use it can ignore it.
