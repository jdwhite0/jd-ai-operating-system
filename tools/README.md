# Tools rack

This folder defines the **default agent toolchain** for JD AI OS.

It is inspired by a desktop “tools rack” pattern (shortcuts to real apps), but ships as **manifests + install scripts** — not proprietary app aliases.

## Required for agent web work

| Tool | Why | Docs |
|------|-----|------|
| **EgoLite** (`ego-browser`) | Best browser for AI agents with real login state | [egolite/README.md](egolite/README.md) |

## Required CLI stack

Defined in [`../toolchain/INSTALL_SEQUENCE.yaml`](../toolchain/INSTALL_SEQUENCE.yaml):

Git · Node · GitHub CLI · Vercel CLI · FFmpeg/FFprobe · Python 3 · editor (Cursor or VS Code)

## Recommended (optional)

| Tool | Why |
|------|-----|
| Obsidian | Human UI over `os/` as a vault |
| Ollama | Local LLM runtime |
| whisper.cpp | Local transcription |

## Explicitly NOT part of default install

Quo · KuCoin · GeckoTerminal · ACCESS product PWAs · Slack/Notion/Render as required deps

See [`desktop-rack.yaml`](desktop-rack.yaml) for the full include/exclude map.
