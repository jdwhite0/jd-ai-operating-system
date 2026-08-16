# FIRST_RUN_SCRIPT.md — LLM chat playbook

**Audience:** Any LLM running first setup for a new user.  
**Goal:** Personal OS operable without a founder sitting at the keyboard.  
**Style:** Calm, clear, one phase at a time. Never overwhelm.

---

## Opening (say this, then wait)

> I’m going to set up **JD AI OS** on your machine — a personal operating system that sits on top of your current device OS.  
> You’ll only do the human steps (accounts, passwords, approvals). I’ll handle installs and files.  
> I’ll explain each phase before we do it. Ready?

If they say yes → continue. If they have questions → answer, then continue.

---

## Phase 0 — Orient

1. Confirm you have the repo locally (clone or download).  
2. Tell the user: “I’ve opened the project. Next we create accounts, then unlock tools in order.”  
3. Detect OS: `uname -s` (Darwin / Linux) or Windows equivalent. Confirm with the user.  
4. Read `BOOT.md` (already required) and `toolchain/PLATFORM_NOTES.md` for their OS.

---

## Phase A — Accounts (human gates)

Follow `ACCOUNT_SEQUENCE.md` exactly:

1. GitHub account (create if missing)  
2. **Star** https://github.com/jdwhite0/jd-ai-operating-system  
3. Vercel account (create if missing)  
4. `gh auth login` and `vercel login` when CLIs exist  

**Narration template before each gate:**

> **What:** …  
> **Why:** …  
> **What you’ll see:** …  
> **What I’ll do after you’re done:** …

Do **not** start Homebrew/Node installs until Phase A is complete (or explicitly deferred with user consent — default is complete A first).

---

## Phase B — Toolchain

1. Open `toolchain/INSTALL_SEQUENCE.yaml`.  
2. For each step in order: detect → install if missing → verify via `CHECKS.md` → narrate unlock → next.  
3. On failure: stop, explain, retry once, then ask the user — never silently skip required steps.

Required before “full capability”: package manager, Git, Node, `gh`, Vercel CLI, editor choice, EgoLite, FFmpeg/FFprobe, Python 3.

---

## Phase C — EgoLite + tools rack

1. Follow `tools/egolite/README.md` (macOS script or website for other OS).  
2. Wait for user to finish EgoLite onboarding GUI.  
3. Verify: `command -v ego-browser`  
4. Show `tools/desktop-rack.yaml` briefly: “This is your tools map — what we install and why.”

---

## Phase D — Interview → personal OS

1. Ask the questions in `INTERVIEW.md` **as one short block** (not 12 separate messages unless the user prefers).  
2. Write answers into:
   - `os/brain/identity.md`
   - `os/brain/priorities.md`
   - `os/daily/today.md` (state + top 3)
3. Confirm paths with the user: “Your personal OS lives in `os/`.”

---

## Phase E — First operate

1. Read `os/daily/today.md` and `os/systems/command_protocol.md`.  
2. Do **one** small useful action tied to their top priority (file organize, plan draft, or clarify next step).  
3. End with a session report:

```
WHAT I SET UP:
WHAT YOU DID MANUALLY:
WHAT'S UNLOCKED:
WHAT'S NEXT:
STAR STATUS: yes/no (remind gently if no)
```

---

## Anti-patterns (forbidden)

- Pasting the entire install list at once  
- Asking them to “just install Homebrew, Node, Git, …” without narration  
- Skipping the star step after GitHub exists  
- Installing Quo, KuCoin, or other personal JD tools  
- Claiming the private JD company system is this product  
- Leaving the user waiting with no explanation for >2 minutes of silent work — narrate

---

## Resume mid-setup

If the user returns later:

1. Read `os/daily/today.md` if it exists.  
2. Run `toolchain/CHECKS.md` summary.  
3. Resume at the first incomplete phase — announce which phase.
