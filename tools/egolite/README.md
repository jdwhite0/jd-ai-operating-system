# EgoLite — agent browser for JD AI OS

**EgoLite** is the preferred browser for AI agents doing real web work with your login state.

Binary after install: `ego-browser`

Official site: https://lite.ego.app/

---

## Why it is required

Agents that open the default system browser often hit login walls. EgoLite keeps an agent-usable browser session so OAuth and authenticated sites work without blind copy-paste into Brave/Chrome.

---

## Install (macOS)

From the repo root:

```bash
sh tools/egolite/install.sh
```

Then finish the **EgoLite onboarding GUI**. Ensure `~/.local/bin` is on your PATH:

```bash
export PATH="$HOME/.local/bin:$PATH"
command -v ego-browser
```

### Other platforms

Use https://lite.ego.app/ for Windows/Linux installers when the shell script does not apply. Do not invent unofficial download URLs.

---

## Usage contract (agents)

1. Prefer `ego-browser` for Discord, OAuth, developer portals, and any login-gated site.
2. Do **not** tell the user to paste authorize URLs into the default browser when EgoLite is available.
3. Narrate before launching: what site, why EgoLite, what the user may need to approve.
4. Smoke test:

```bash
ego-browser nodejs <<'EOF'
console.log('ego-browser ready')
EOF
```

### Minimal task pattern

```bash
ego-browser nodejs <<'EOF'
const task = await useOrCreateTaskSpace('short goal name')
await openOrReuseTab('https://example.com', { wait: true, timeout: 45 })
// interact within this space
EOF
```

Exact APIs evolve with EgoLite — if a helper is missing, read EgoLite docs and adapt. Never fall back to “open in default browser” for authenticated flows when EgoLite is installed.

---

## Human gates

- First launch / onboarding wizard  
- macOS Gatekeeper approval  
- Signing into sites inside EgoLite (user’s accounts stay theirs)

---

## Privacy

EgoLite runs on the user’s machine with the user’s sessions. JD AI OS does not receive those credentials. Treat the browser like any personal browser.
