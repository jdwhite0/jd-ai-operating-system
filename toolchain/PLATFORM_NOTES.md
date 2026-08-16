# PLATFORM_NOTES.md

Guidance for agents installing the toolchain across operating systems.

---

## macOS (primary)

- Prefer **Homebrew** for Git, Node, `gh`, FFmpeg, Python.
- EgoLite: `sh tools/egolite/install.sh` then finish onboarding GUI.
- Apple Silicon: brew often lives at `/opt/homebrew/bin` — ensure PATH.
- Gatekeeper: user may need to approve downloaded apps (Cursor, EgoLite, Obsidian).

---

## Linux

- Use distro package manager (`apt` / `dnf` / `pacman`) when brew is unavailable.
- Node: prefer NodeSource or official LTS packages if distro Node is too old (<20).
- EgoLite: point user to https://lite.ego.app/ for supported builds; do not invent install paths.
- `gh` and `vercel` still required once accounts exist.

---

## Windows

- Prefer **winget** for Git, Node LTS, GitHub CLI, VS Code, FFmpeg, Python.
- EgoLite: https://lite.ego.app/ — follow official Windows instructions.
- PowerShell vs CMD: prefer PowerShell for modern CLIs.
- WSL2 is optional; if used, run Linux sequence inside WSL and keep Windows GUI apps on Windows.

---

## Universal rules

1. Detect before install.
2. Narrate why each tool matters.
3. One required unlock at a time.
4. Stop at human gates (signup, 2FA, OAuth, Gatekeeper).
5. Do not install excluded apps (Quo, KuCoin, ACCESS PWA, etc.) — see `INSTALL_SEQUENCE.yaml`.
6. Optional tools (Obsidian, Ollama, whisper) only after required path is green.
