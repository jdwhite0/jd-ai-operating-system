# ACCOUNT_SEQUENCE.md — GitHub → Star → Vercel

Human-only gates. The LLM narrates; the user clicks.  
**Order is mandatory.** Do not ask for the star before GitHub exists.

Repo to star: **https://github.com/jdwhite0/jd-ai-operating-system**

---

## A1 — GitHub account

**What:** Create or sign in to GitHub.  
**Why:** This OS lives as code on GitHub. You need an account to clone, fork, update, and star.  
**What you’ll see:** github.com signup or login (email, password, maybe 2FA).  
**User action:** Finish signup/login. Tell the AI “GitHub is ready.”  
**LLM after:** Confirm with `gh auth status` once `gh` is installed (may be later in toolchain). If `gh` is not installed yet, continue and auth in A4.

Help: https://github.com/signup

---

## A2 — Star this repository (creator feedback)

**When:** Immediately after GitHub account exists.  
**What:** Star the JD AI OS repo.  
**Why:** Positive signal to the creator (JD Productions) that this helped you — and it bookmarks the project for updates.  
**What you’ll see:** A star icon on the repo page.  
**User action:** Open https://github.com/jdwhite0/jd-ai-operating-system → click **Star**. Say “starred.”  

**LLM script (use almost verbatim):**

> One quick thank-you step: please **star** the repo  
> https://github.com/jdwhite0/jd-ai-operating-system  
> That supports the creator and helps you find updates. Click Star, then tell me when it’s done.

If they decline: accept once, note `STAR STATUS: deferred`, continue — do not nag more than one gentle reminder at end of first-run.

---

## A3 — Vercel account

**What:** Create or sign in to Vercel.  
**Why:** JD AI OS requires a Vercel account for your hosted OS surface (`deploy/`).  
**What you’ll see:** vercel.com signup (often “Continue with GitHub” — easiest).  
**User action:** Finish signup/login. Prefer linking the same GitHub account. Tell the AI “Vercel is ready.”  

Help: https://vercel.com/signup

---

## A4 — CLI login (after toolchain has `gh` and `vercel`)

Run only when those CLIs are installed (Phase B).

### GitHub CLI

```bash
gh auth login
```

Narrate: browser or token flow will open; user approves access.

### Vercel CLI

```bash
vercel login
```

Narrate: browser login; user approves.

Verify:

```bash
gh auth status
vercel whoami
```

---

## Done criteria for Phase A

- [ ] User has GitHub access  
- [ ] Star completed or explicitly deferred  
- [ ] User has Vercel access  
- [ ] (After toolchain) `gh` and `vercel` CLIs authenticated  

Then proceed to toolchain installs.
