---
tags: [component, Nasema_pharmacy_Hall]
---
- Path: `.github/workflows/deploy.yml`
- Role: GitHub Actions workflow that publishes the repo root to GitHub Pages on push to `main` or manual `workflow_dispatch`; checks out the repo, configures Pages (`enablement: true`), uploads `.` as the Pages artifact, and deploys it (deploy.yml:1-38).
- Talks to: [[ShowcasePage]]
- Back: [[ARCHITECTURE]]
