# Akwaaba Learning Garden

Marketing site + installable PWA for Akwaaba Learning Garden — a crèche, nursery & primary school in Accra.

## Stack

Static HTML/CSS/JS, no build step. Ships as a Progressive Web App (offline-capable via service worker).

| File | Purpose |
|------|---------|
| `index.html` | The entire site (inline CSS/JS) |
| `manifest.json` | PWA install manifest |
| `sw.js` | Service worker (stale-while-revalidate caching) |
| `icons/` | App icons (192px, 512px) |

## Deployment

Deployed on **Cloudflare Pages** with Git integration — every push to `main` triggers an automatic production deploy. No build command; output directory is the repo root (`/`).

## Local preview

Because the service worker requires a server (not `file://`), run any static server:

```bash
npx serve .
# or
python -m http.server 8000
```
