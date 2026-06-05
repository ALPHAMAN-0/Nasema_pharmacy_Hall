# Nasema Pharmacy — showcase site (deploy bundle)

This folder is a **ready-to-deploy GitHub Pages site** showcasing the Nasema Pharmacy
desktop app. Drop its **contents** into a separate GitHub repo and the page goes live
automatically — no build step.

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
   (i.e. `index.html` must be at the root, not inside a sub-folder.)
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
- The page is a **portfolio showcase** (the app is not open source, and there's no public download).
  The only outbound link is **View on GitHub**, pointing to the app's code repo
  `https://github.com/NextByte-Solutions/Pharmacy_Nasima_Medical_Hall`. If that repo is **private**,
  remove the "View on GitHub" buttons (one in the nav, one in the hero) before publishing.
- The **Location** section embeds a Google Map (the pharmacy at 23°45'59.4"N 90°21'35.2"E). It needs
  internet to display and only renders when the page is viewed online (e.g. on GitHub Pages),
  not from a local file.
- To update the site later, edit `index.html`, commit, and push — Pages redeploys automatically.
