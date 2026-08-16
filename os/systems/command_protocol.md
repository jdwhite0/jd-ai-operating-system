# Command Protocol — Master Operating Rules

> The master rules for this system. Any AI working here follows these. Read before writing anything.

---

## 1. The core loop

```
BOOT.md → os/daily/today.md → os/systems/ → os/brain/ → act → report
```

Always check `os/daily/today.md` first. The execution state controls what you should do.

## 2. File rules

1. **Read before writing.** Never assume a file's contents or structure — open it.
2. **Append, don't overwrite.** Preserve history. Note what changed if you replace content.
3. **One source of truth.** Update the canonical file in `os/brain/`. Never duplicate.
4. **Never delete** without explicit permission.
5. **If unsure of a path, search — never guess.** Never hallucinate paths or logic.

## 3. Where things go

| If it's... | It goes in... |
|------------|---------------|
| A lasting fact about you or a domain | `os/brain/` |
| A rule about how the system runs | `os/systems/` |
| Today's state or tasks | `os/daily/today.md` |
| Active project work | `os/projects/<project>/` |
| Photos / video / exports | `os/media/` |
| Reference material | `os/resources/` |
| A script / automation | `os/automations/` |
| Scratch / disposable | `os/temp/` (create as needed) |

## 4. Task rules

- Respect the priority ladder (P0–P3 / Someday). See [`task_rules.md`](task_rules.md).
- Never more than **3 P0s** at once.
- Match your behavior to the current execution state. See [`execution_states.md`](execution_states.md).

## 5. End every session with a report

State plainly: what you did, what you did **not** do, and what needs a decision next.
Don't overstate. If something failed, say so.

## 6. Multiple AIs

See [`ai_rules/ai_collaboration.md`](ai_rules/ai_collaboration.md) so different assistants
don't step on each other.
