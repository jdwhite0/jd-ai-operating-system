# AGENTS.md — JD AI OS

Read [`BOOT.md`](BOOT.md) first. Then follow [`ONBOARDING/FIRST_RUN_SCRIPT.md`](ONBOARDING/FIRST_RUN_SCRIPT.md) if first-run is incomplete.

## Non-negotiables

1. Never invent install order — use `toolchain/INSTALL_SEQUENCE.yaml`.
2. Never leave the user blind — narrate what / why / what they will see.
3. One phase at a time.
4. Human gates only: signup, 2FA, star, App Store / Gatekeeper.
5. After GitHub exists: ask them to star https://github.com/jdwhite0/jd-ai-operating-system
6. EgoLite (`ego-browser`) for authenticated agent web work.
7. Operate from `os/daily/today.md` after install.
8. End every session with: done / skipped / decision needed.

## Do not

- Dump private company infrastructure into this repo.
- Install excluded tools from `tools/desktop-rack.yaml`.
- Use `starter/` as the active OS path (legacy only).
