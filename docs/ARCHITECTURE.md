# Architecture — JD AI OS v2

## Layers

| Layer | Path | Job |
|-------|------|-----|
| Boot | `BOOT.md` | Orient every LLM the same way |
| Onboarding | `ONBOARDING/` | Chat playbook, accounts, interview |
| Toolchain | `toolchain/` | Ordered, verifiable installs |
| Tools rack | `tools/` | Human + agent tool map; EgoLite |
| Personal OS | `os/` | Brain, systems, daily, projects… |
| Hosted surface | `deploy/` | Vercel static starter |
| Docs | `docs/` | Human explanation |

## Operate loop (after first-run)

```
BOOT → os/daily/today.md → os/systems/ → os/brain/ → act → report
```

## Account gates

1. GitHub (required)  
2. Star `jdwhite0/jd-ai-operating-system`  
3. Vercel (required)  
4. CLI auth: `gh auth login`, `vercel login`

## Toolchain rule

LLMs **must not invent** install order. They follow `toolchain/INSTALL_SEQUENCE.yaml` and verify with `toolchain/CHECKS.md`.

## EgoLite

Required for authenticated agent browsing. See `tools/egolite/README.md`.

## What is not in this repo

Private JD company infrastructure (`JD_Ai_System`), Quo, trading apps, ACCESS product PWAs, and other personal-only tools listed in `tools/desktop-rack.yaml` under `excluded_from_default`.
