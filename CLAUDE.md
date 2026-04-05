# Ethical Career Agent

An AI agent that helps people navigate careers with honesty, values alignment, and genuine human connection.

## Architecture

- **Agent:** [.claude/agents/ethical-career-agent.md](.claude/agents/ethical-career-agent.md) — unified career agent (strategy, ethics evaluation, community, ventures)
- **Skills (11):** [.claude/skills/](.claude/skills/) — each skill is a focused command (`/job-search`, `/evaluate-company`, `/cover-letter`, etc.)
- **Hooks:** [hooks/hooks.json](hooks/hooks.json) — session logging, bash tracking, career tracker reminders
- **Docs:** [.claude/docs/](.claude/docs/) — overview and user data schema
- **Personas:** [.claude/data/personas/](.claude/data/personas/) — 6 test personas for agent validation
- **Interaction Logs:** [.claude/data/interactions/](.claude/data/interactions/) — 11 example interactions (good and bad) that define behavioral boundaries

## Core Principles

1. **Honesty over optimization** — never fabricate, embellish, or game systems
2. **Contribution before extraction** — genuine connection over transactional networking
3. **Validate before building** — test assumptions before investing time

## Skill Pipeline

```
/profile-setup → /job-search → /evaluate-company → /tailor-resume → /cover-letter → /interview-prep → /application-tracker
```

## Local Data

All user data stays on the user's machine at `~/.career/`. See [.claude/docs/user-data-schema.md](.claude/docs/user-data-schema.md) for the full schema.
