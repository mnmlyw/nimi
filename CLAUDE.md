# nimi

Toki Pona flashcard app.

## Structure

- `index.html` — Single-file app (HTML + CSS + JS, no build step)
- `manifest.json` — App manifest
- `sw.js` — Service worker for offline support
- `icon.svg` — App icon

## Key details

- 120 core pu words + 19 extended nimi sin (toggled via header switch)
- Word data is inline in `index.html` as `PU` and `KU` arrays
- State persisted in localStorage: theme (`tp-theme`), seen words (`tp-seen`), extended toggle (`tp-ext`)
- Service worker uses stale-while-revalidate; bump `CACHE` version in `sw.js` on updates
- Fonts: Cormorant Garamond (display) + Outfit (UI) via Google Fonts

## Deploy

- Hosted on GitHub Pages: https://mnmlyw.github.io/nimi/
- Pushes to `main` auto-deploy
