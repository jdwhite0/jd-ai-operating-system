# AI Collaboration Rules

> You may connect more than one AI to this system (Claude, ChatGPT, Gemini, etc.).
> These rules keep them aligned and stop them from undoing each other's work.

---

## Universal rules (every AI)

1. **Orient first.** Read `BOOT.md`, then `os/daily/today.md`, then the relevant `os/brain/` file.
2. **One source of truth.** Truth lives in `os/brain/`. Don't create competing versions.
3. **Append, don't overwrite.** Preserve what others have written.
4. **Leave a trace.** When you change a system or brain file, note it (date + what changed).
5. **Stay in your lane.** Do the task asked. Don't silently restructure the system.
6. **Never delete** without explicit permission.
7. **Report at the end** — what you did, skipped, and what needs a decision next.

## Handoff note

When a session meaningfully changes the system, add a one-line note at the bottom of
`os/daily/today.md` under **"AI log"**:

```
AI log:
- 2026-08-16 (Claude): set up the system skeleton.
```

## Hierarchy of truth (highest first)

1. The owner (a direct instruction always wins)
2. `os/brain/` (source of truth)
3. `os/systems/` (the rules)
4. `os/daily/today.md` (current state)
5. The AI's own reasoning (lowest)

If your reasoning conflicts with anything above it, defer — or ask.

---

*The system is the shared contract. Every AI honors it.*
