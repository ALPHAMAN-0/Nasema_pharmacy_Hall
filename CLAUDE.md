# CLAUDE.md — Nasema_pharmacy_Hall

## Build / test / lint
- None found — no package manager or manifest in this repo. Static file, "no build step" (README.md:5).

## Rules observed
- `index.html` must be at the deploy target's repo root, not inside a sub-folder (README.md:20).
- No build step: update the live site by editing `index.html` directly, then commit and push to `main` — Pages redeploys automatically (README.md:42).
- This folder is a deploy bundle for a *separate* GitHub repo (e.g. `nasema-showcase`), not the app's own source (README.md:1-5, 14-20).

## Files worth reading first
1. `index.html` — the entire site (markup, CSS, JS)
2. `README.md` — deploy-bundle instructions and notes
3. `.github/workflows/deploy.yml` — GitHub Pages publish workflow

Architecture: see ARCHITECTURE.md — read before structural changes
