# Architecture — JD AI OS

JD AI OS is a **folder-based operating system** for your life and work. It's designed so
that any AI assistant can plug in, orient itself in under two minutes, and operate
consistently from your real data.

---

## The Core Loop

```
AI_START_HERE → today's state → system rules → your brain (truth) → act → report
```

Every AI session follows the same path. This is what makes the system *consistent* no
matter which assistant is driving — Claude today, ChatGPT tomorrow, something new next year.

---

## The Layers

### 🧠 Brain — Source of Truth (`01_BRAIN/`)
Who you are and what's true. Identity, priorities, and one file per life/work domain
(finances, health, ventures). AI reads from here; it never invents facts that contradict it.

### ⚙️ Systems — Operating Rules (`02_SYSTEMS/`)
The rules that make the system run the same way every time: the command protocol,
execution states, task rules, and AI-collaboration rules so multiple assistants don't
step on each other.

### ❤️ Daily — Current State (`03_DAILY/`)
`today.md` is the heartbeat. It holds your current **execution state**, energy, and task
list. The state controls how AI behaves today.

### 🚀 Projects (`04_PROJECTS/`)
One folder per project or venture. New businesses drop in here without restructuring anything.

### Support layers
- `05_MEDIA/` — raw, exports, archive
- `06_RESOURCES/` — reference libraries
- `07_AUTOMATIONS/` — scripts that maintain the system
- `08_BACKUPS/` — snapshots of the irreplaceable parts

---

## Execution States

The state in `today.md` tells every AI how to behave:

| State | Meaning | AI behavior |
|-------|---------|-------------|
| 🔴 Focus | Deep work | Terse. Critical tasks only. |
| ⚡ Execution | Clearing the list | Action-oriented. |
| 🌱 Growth | Learning | Creative input welcome. |
| 🗺️ Planning | Strategy | Help organize. |
| 🔋 Recovery | Low energy | Brief. Light tasks only. |

This protects the human and keeps the AI aligned with how they're *actually* operating.

---

## Design Principles

1. **Plain files, your machine.** No cloud lock-in. You own everything.
2. **One source of truth.** Truth lives in the brain; no competing copies.
3. **AI-agnostic.** A universal boot file orients any assistant.
4. **Read before writing.** Agents never assume; they verify.
5. **Built to scale.** New ventures slot in via templates — the system grows with you.
