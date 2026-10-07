# claude-brain-starter

A minimal file-based memory structure for Claude Code. Three layers, works on day one.

```
CLAUDE.md                 router: who you are, what's burning, where things live (≤60 lines)
core/preferences.md       how Claude should talk to you
core/open-loops.md        what's waiting on a decision
spheres/<name>/CLAUDE.md  one hub per real area of life/work
checkpoints/              one note per session: "start tomorrow with…"
```

## How it works
Claude Code auto-loads `CLAUDE.md` from the folder you start it in (and its parents). The root file stays small and *routes*; details live in sphere hubs, loaded only when you work inside that folder. This keeps context lean.

## Rules that make it work
1. Root `CLAUDE.md` ≤ 60 lines. Overflow goes to a hub.
2. A sphere is created when it's real, not in advance.
3. Every session ends with one line: what you start with next time.
4. Decisions get written down with a date, so you stop re-arguing them.

## Level 2 — only when you hit the wall
- **Hooks** (`settings.json`) — inject reminders on prompt submit / session start.
- **Skills** — reusable workflows (checkpoint, weekly memory sync).
- **Decisions index** — when hubs accumulate many decisions, generate a short index.

Don't build these up front. Add each one when you feel the specific pain it solves.

Русский quickstart — [QUICKSTART.ru.md](QUICKSTART.ru.md).
