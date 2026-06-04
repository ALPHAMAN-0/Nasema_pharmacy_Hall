# Nasema Pharmacy — showcase site (deploy bundle)

This folder is a **ready-to-deploy GitHub Pages site**. Drop its **contents** into a
separate GitHub repo and the page goes live automatically — no build step.

## What's inside
```
index.html                      ← the whole showcase site (one self-contained file)
.github/workflows/deploy.yml    ← publishes to GitHub Pages on every push to main
```

## Deploy to a separate repo
1. Create a new repo on GitHub — e.g. `nasema-showcase` (it can be empty).
2. Copy the **contents of this folder** into that repo so the **repo root** looks like:
   ```
   index.html
   .github/workflows/deploy.yml
   ```
   (i.e. `index.html` must be at the root, not inside `DeploymentFIle/`.)
3. Commit & push to `main`:
   ```bash
   git add index.html .github/workflows/deploy.yml
   git commit -m "Add Nasema Pharmacy showcase site"
   git push origin main
   ```
4. In that repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
   (The workflow also sets `enablement: true`, so it tries to turn Pages on by itself —
   but flipping this once is the reliable fix if the first run says *"Get Pages site failed"*.)
5. The **Actions** tab shows the deploy. Once green, the site is live at:
   - **Project repo** (e.g. `nasema-showcase`): `https://<your-username>.github.io/nasema-showcase/`
   - **User/Org site** (repo named exactly `<your-username>.github.io`): `https://<your-username>.github.io/`

## Notes
- The links inside the page (View on GitHub, Download) point to the **app's code repo**:
  `https://github.com/NextByte-Solutions/Pharmacy_Nasima_Medical_Hall` — that stays the same
  no matter where the site is hosted.
- To update the site later, edit `index.html`, commit, and push — Pages redeploys automatically.
