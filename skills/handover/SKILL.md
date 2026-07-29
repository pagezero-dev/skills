---
name: handover
description: >-
  Produce a copy-pasteable context summary of the current chat so a new AI agent
  can continue the work. Use only when the user explicitly asks for a handover,
  handoff, context summary for a new chat, or invokes /handover.
disable-model-invocation: true
---

# Handover

Create a **single copy-pasteable block** the user can paste into a new chat. Do not write it to a file unless asked. Do not continue the original task after producing the summary.

## Workflow

1. Infer state from this conversation only (plus quick facts you already know: branch, open files, recent edits). Do not run a broad codebase exploration just for the summary.
2. Prefer concrete paths, commands, decisions, and next actions over narrative.
3. Omit secrets, tokens, credentials, and full dumps of large logs or diffs.
4. Output **only** the handover block below (plus a one-line note that it is ready to paste). No preamble essay.

## Output template

Use this structure. Drop a section only if it would be empty; keep headings otherwise so the next agent can scan quickly.

```markdown
# Handover

## Goal
<What the user is trying to achieve>

## Done
- <Completed work, with file paths where relevant>

## In progress
- <Partially done work and current state>

## Next steps
1. <Immediate next action for the new agent>
2. <…>

## Key decisions
- <Choices already made and constraints to respect>

## Relevant paths
- `path/to/file` — <why it matters>

## Commands / state
- Branch: `<name>`
- <Important commands already run, failing tests, env notes — no secrets>

## Open questions / blockers
- <Unresolved questions or blockers, or "None">
```

## Quality bar

- Next agent should be able to start without re-reading this chat.
- Next steps must be actionable and ordered.
- Paths and symbols must be accurate; if unsure, say so under Open questions.
