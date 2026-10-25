# 01 — Scaffold the PWA and deploy to GitHub Pages

Status: ready-for-agent
Blocked by: —
Spec: `../spec.md`

## What to build

An empty but installable app shell, live at a public URL. Set up Vite + React + TypeScript with Vitest. Add `vite-plugin-pwa` (manifest named "Snus Quit", generated green icon, standalone display, offline service worker). Build a mobile layout that follows the system light/dark setting, with a bottom tab bar (Today, Progress, Milestones, Settings) whose tabs are placeholders for now. Add a GitHub Actions workflow that builds and deploys to GitHub Pages, with the right base path.

**Confirm with the user before creating the public GitHub repo** under `saitoharuki-git` and pushing. That step publishes the code.

## Acceptance criteria

- [ ] `npm run dev`, `npm run build` and `npm test` all work (one placeholder test is fine)
- [ ] The four tabs switch between placeholder screens; the layout looks right at iPhone width in light and dark mode
- [ ] The public repo exists and pushing to `main` deploys to GitHub Pages
- [ ] The deployed site can be added to the iPhone home screen, opens full-screen with the icon and name, and loads offline
