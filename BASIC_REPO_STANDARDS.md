# Basic Repo Standards Report

**Repo:** `lokal-app/frontend-web-template` (renamed from `react-webview-template`)
**Date:** 2026-10-28

## 1. Projects

Single project: a React 19 + Vite 8 + Tailwind CSS v4 starter template (JavaScript/JSX, Oxlint). No workspaces or sub-apps.

## 2. README.md

- **Found:** Real content, but titled "React Webview Template" with the old `degit` path, no tech-stack or scripts section, and leftover Vite boilerplate about the two React plugins.
- **Fixed:** Renamed to "Frontend Web Template", updated the `degit` command to `lokal-app/frontend-web-template`, and added Tech Stack, Scripts and Environment Variables sections. Removed the Vite plugin boilerplate.

## 3. CLAUDE.md

- **Found:** Present and project-specific. The goal statement was there, but it came after the title and the "Do not edit" note instead of first.
- **Fixed:** Moved the goal statement to the top of the file as a quote block. The rest of the file is unchanged.

## 4. .gitignore / env files

- **Found:** `.gitignore` covered `.env` only. There was no `.env.example`. No env files are tracked, and the code doesn't read `import.meta.env`.
- **Fixed:** Added `.env.*` and `!.env.example` to `.gitignore`. Added a `.env.example` that says no variables are required and explains the `VITE_` prefix.

## 5. GitHub Actions

- **Found:** No `.github/workflows/`. `master` is the only branch on the remote; there is no separate dev or staging branch.
- **Fixed:** Added `.github/workflows/ci.yml`, which runs `npm ci`, `npm run lint` and `npm run build` on Node 22 for pushes and pull requests to `master`. If a dev or staging branch is created later, add it to the workflow.

## Other changes and open items

- Renamed the package in `package.json` and `package-lock.json` (the lockfile still said `claude-fe-ai-playground`) and the page `<title>` in `index.html` to match the new repo name.
- Removed the unused `bin` entry from `package.json`. It pointed to `bin/create.js`, which never existed. Scaffolding works through `npx degit`.
- There is no test suite.
