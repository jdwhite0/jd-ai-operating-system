# BOOT.md — Read this first

**For every LLM:** Before installing, interviewing, or operating anything, read this file completely. Then follow `ONBOARDING/FIRST_RUN_SCRIPT.md` in order.

**For humans:** You do not need to memorize this. Your AI will walk you through it. This file exists so any model (Claude, ChatGPT, Gemini, Cursor, local) behaves the same way.

---

## What JD AI OS is

A **personal operating system** that sits on top of your device OS (macOS, Windows, or Linux). Plain files you own. Any LLM you choose can operate it.

It is **not** a notes dump. It is not someone else’s cloud brain. It is your machine + your rules + your memory.

## What you need (accounts)

| Account | Why |
|---------|-----|
| **GitHub** | Home for this repo, updates, and your fork |
| **Vercel** | Deploy path for your hosted OS surface |

After your GitHub account exists, **star this repository**:  
https://github.com/jdwhite0/jd-ai-operating-system  

That tells the creator the system is helping people — and helps you track updates.

## UX laws (LLM must obey)

1. **Never leave the user blind** — before each step, say what / why / what they will see.  
2. **Never dump a wall of tasks** — one phase at a time; celebrate progress.  
3. **LLM does the heavy work** — installs, file writes, checks.  
4. **Human gates only for the user** — signups, 2FA, starring, App Store / Gatekeeper prompts.  
5. **Teach in public** — the user should learn the stack by watching it unlock.  
6. **Never invent install order** — follow `toolchain/INSTALL_SEQUENCE.yaml`.  
7. **Report at the end of every session** — what you did, skipped, and what needs a decision.

## First-run order (do not skip)

1. `ONBOARDING/FIRST_RUN_SCRIPT.md` — full playbook  
2. `ONBOARDING/ACCOUNT_SEQUENCE.md` — GitHub → **star** → Vercel  
3. `toolchain/INSTALL_SEQUENCE.yaml` + `toolchain/CHECKS.md`  
4. `tools/egolite/README.md` — agent browser  
5. `ONBOARDING/INTERVIEW.md` — short Q&A → write `os/`  
6. Operate from `os/daily/today.md`

## Repo map

| Path | Role |
|------|------|
| `BOOT.md` | This file — universal entry |
| `ONBOARDING/` | Chat playbook, accounts, interview |
| `toolchain/` | Ordered installs + verification |
| `tools/` | Human-visible tools rack + EgoLite |
| `os/` | Your personal OS (brain, systems, daily) |
| `deploy/` | Vercel starter for hosted surface |
| `docs/` | Architecture, FAQ, philosophy |
| `starter/` | Legacy v1 path — **use `os/` instead** |

## Operate loop (after install)

```
BOOT → os/daily/today.md → os/systems/ → os/brain/ → act → report
```

---

*JD AI OS · https://github.com/jdwhite0/jd-ai-operating-system · by JD Productions*
