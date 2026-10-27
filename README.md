# Nikki Project Manager (Cloudflare)

A lightweight personal kanban board. Add tasks, tag them with a project, move them between **To do → In progress → Done**, search across everything, and keep free-form project notes underneath the board.

## Features

- Three-column board with task counts
- Task details: title, project, description
- Search across title, project and details
- Project notes area
- Works on phones (columns scroll sideways)
- Installable as a PWA (`manifest.json`)

## How it works

Plain HTML, CSS and JavaScript — no build step, no framework.

| File | What it does |
|---|---|
| `index.html` | Page layout and styles |
| `app.js` | Board logic, rendering and storage |
| `manifest.json` | PWA manifest |
| `wrangler.jsonc` | Cloudflare Pages config (serves the repo root) |

Data is saved in your browser's `localStorage` (key `nikki-project-manager-cloudflare-v1`), so it stays on the device you use and isn't synced.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy

```bash
npx wrangler pages deploy . --project-name nikki-project-manager-cloudflare
```
