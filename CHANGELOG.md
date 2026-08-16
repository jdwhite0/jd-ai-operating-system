# Changelog

## 2.0.0 — 2026-08-16

### Product

- Repositioned as a **universal open-source personal OS** on top of any device OS.
- Chat-first first-run: retrieve repo → accounts → toolchain → EgoLite → interview → operate.
- **GitHub + Vercel required**; star this repo after GitHub exists.
- MIT license (with trademark note).

### Added

- `BOOT.md` — universal LLM entry
- `ONBOARDING/` — `FIRST_RUN_SCRIPT.md`, `ACCOUNT_SEQUENCE.md`, `INTERVIEW.md`
- `toolchain/` — `INSTALL_SEQUENCE.yaml`, `CHECKS.md`, `PLATFORM_NOTES.md`
- `tools/` — tools rack + EgoLite install + usage contract
- `os/` — personal OS skeleton (replaces v1 `starter/` as the active path)
- `deploy/` — Vercel static starter
- Root `AGENTS.md` / `CLAUDE.md` pointing at `BOOT.md`

### Changed

- README and docs rewritten for the personal OS product (not chief-of-staff marketing alone).
- `starter/` retained as legacy redirect to `os/`.

### Removed / excluded from default

- Proprietary-only framing for the public starter
- Personal/JD-only apps as required installs (Quo, trading PWAs, ACCESS, etc.)

---

## 1.0.0 — 2026-06-16

Initial public release: Markdown second-brain starter under `starter/`, proprietary license, marketing as AI chief-of-staff.
