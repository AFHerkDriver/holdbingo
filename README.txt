HOLD / BINGO — installable offline web app
==========================================

WHAT'S IN HERE
  index.html ............ the app
  manifest.webmanifest .. makes it installable
  sw.js ................. service worker (offline caching)
  apple-touch-icon.png .. Home Screen icon (180px)
  icon-192.png / icon-512.png .. manifest icons

INSTALL (one-time)
  1. Host this folder at an HTTPS URL. Easiest options:
       - Netlify Drop: open app.netlify.com/drop in Safari and
         drag this whole folder onto the page. You get a live
         https://....netlify.app link in seconds. (No account needed.)
       - or GitHub Pages: upload these files to a repo, then
         Settings > Pages.
     NOTE: the folder must keep index.html at its top level.
  2. Open the URL in SAFARI (not Chrome). Wait ~2 sec.
  3. Share > Add to Home Screen > Add.

USE
  Tap the new icon. It launches full screen and runs fully
  offline after the first load — clock, countdown, 757/767
  presets, bingo readout, everything.

UPDATING LATER
  Re-deploy the updated folder. If the app doesn't refresh on
  your iPhone/iPad, delete the Home Screen icon and Add to
  Home Screen again to clear the old cache.
