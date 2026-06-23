# Hold / Bingo Calculator

**Version 1.0** · Installable, offline-first EFB tool for the 757 / 767.

**Live:** https://afherkdriver.github.io/holdbingo/
*(URL assumes the repo is named `holdbingo`; if you name it something else, the path changes to match.)*

---

## What it does

A holding / bingo decision tool that answers two questions at a glance: **how long can I hold**, and **what fuel and clock time forces me to leave for my divert**.

- **Aircraft presets** — tap `757` or `767` to load that fleet's Min fuel, Emergency fuel, Final approach, and GA & return numbers. `MANUAL` for anything custom.
- **Core math** — enter fuel on board, hold fuel flow, divert fuel, and reserve floor; it returns **Max hold time**, the **Push time** (Zulu + local), a **live countdown**, and **Bingo fuel** (divert + reserve) as its own large readout.
- **Reserve floor toggle** — `MIN` or `EMERG`, auto-filled per aircraft; the labels track which floor you're protecting.
- **Fuel bar + color states** — splits fuel on board into burnable Hold / Divert / Reserve, and shifts green → amber (~10 min out) → red (below bingo).
- **Optional builders** — derive divert fuel from leg distance / groundspeed / fuel flow plus a Final approach or GA & return chip; derive reserve from minutes × fuel flow.
- **Push alarm** — arm it (one tap, also unlocks iOS audio) for an audible alert at hold-time expiration. Holds the screen awake while armed. Foreground only — iOS won't sound it if the app is backgrounded or the phone is locked, and there's no vibration.
- **Offline** — after the first load it runs with no connection of any kind.

---

## Install (one-time)

The app is served from GitHub Pages, then added to the Home Screen as a web app.

1. Push these files to a GitHub repo (see below) and enable **Settings → Pages** (Source: Deploy from a branch → `main` → `/root`).
2. Open the live URL above in **Safari** (must be Safari) and wait a second for the service worker to register.
3. **Share → Add to Home Screen → Add.**
4. Launch from the icon. It opens full screen and runs entirely offline.

## Deploy to GitHub (web, works from iPad)

1. github.com → **+ → New repository** → name it `holdbingo` (lowercase), Public, Create.
2. On the empty repo, click **uploading an existing file**.
3. Upload these files to the repo **root** (not inside a subfolder):
   `index.html`, `manifest.webmanifest`, `sw.js`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `README.md`.
4. **Commit changes**, then enable Pages as in step 1 above.

Command line alternative:

```
git init
git add .
git commit -m "Hold/Bingo v1.0"
git branch -M main
git remote add origin https://github.com/AFHerkDriver/holdbingo.git
git push -u origin main
```

## Updating later

Re-upload the changed files (or push again). The service worker cache version is bumped on each release so the new version takes; if your installed copy doesn't refresh, delete the Home Screen icon and Add to Home Screen again.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The app (all HTML/CSS/JS inline) |
| `manifest.webmanifest` | Makes it installable |
| `sw.js` | Service worker — offline caching |
| `apple-touch-icon.png` | Home Screen icon (180px) |
| `icon-192.png` / `icon-512.png` | Manifest icons |

---

*Decision support only. Always verify against approved aircraft performance data and fuel reserves.*
