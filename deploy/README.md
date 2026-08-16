# Deploy — Vercel hosted surface

GitHub + Vercel are **required** for JD AI OS first-run.

## First deploy (from this folder)

```bash
cd deploy
vercel login          # if needed
vercel                # link / create project
vercel --prod         # when ready
```

Or from repo root with Vercel project root set to `deploy/`.

## What this ships

- Static starter page at `public/index.html`
- `vercel.json` for a simple static deploy

## After first deploy

Replace `public/index.html` with your own portal, dashboard, or status surface.
Keep secrets out of `public/`.
