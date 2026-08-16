# CHECKS.md — Verify each unlock

Run after installs (or when resuming setup). Narrate results to the user in plain language.

---

## Quick summary command (macOS / Linux)

```bash
echo "=== JD AI OS toolchain check ==="
command -v brew >/dev/null && echo "OK package manager (brew)" || echo "MISSING package manager"
command -v git >/dev/null && echo "OK git $(git --version 2>/dev/null)" || echo "MISSING git"
command -v node >/dev/null && echo "OK node $(node -v)" || echo "MISSING node"
command -v npm >/dev/null && echo "OK npm $(npm -v)" || echo "MISSING npm"
command -v gh >/dev/null && echo "OK gh $(gh --version 2>/dev/null | head -1)" || echo "MISSING gh"
command -v vercel >/dev/null && echo "OK vercel $(vercel --version 2>/dev/null)" || echo "MISSING vercel"
command -v ego-browser >/dev/null && echo "OK ego-browser" || echo "MISSING ego-browser (EgoLite)"
command -v ffmpeg >/dev/null && echo "OK ffmpeg" || echo "MISSING ffmpeg"
command -v ffprobe >/dev/null && echo "OK ffprobe" || echo "MISSING ffprobe"
command -v python3 >/dev/null && echo "OK python3 $(python3 --version 2>/dev/null)" || echo "MISSING python3"
```

If `ego-browser` is missing after EgoLite onboarding:

```bash
export PATH="$HOME/.local/bin:$PATH"
command -v ego-browser
```

---

## Auth checks

```bash
gh auth status
vercel whoami
```

---

## EgoLite runtime smoke test

```bash
ego-browser nodejs <<'EOF'
console.log('ego-browser ready')
EOF
```

Expect: `ego-browser ready`

---

## How to report to the user

> **Unlocked:** …  
> **Still missing:** …  
> **Next step:** …  

Never mark first-run complete while a **required** step from `INSTALL_SEQUENCE.yaml` is missing (unless the user explicitly waives it in writing in chat).
