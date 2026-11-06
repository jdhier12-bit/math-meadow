# Math Meadow
A new standalone math game: no arcade, XP, accounts, ads, or external dependencies.

## Open locally
Run from this directory:

```sh
python3 -m http.server 8080
```

Open http://localhost:8080 in your browser. No build or install is needed.
Directly opening index.html works for practice, but service workers and installation require localhost or HTTPS.

## Play
Choose multiplication or division and a 2–5 digit number. The second factor/divisor is 2–9 to keep practice approachable. Division always has a whole-number answer. Multiplication uses a vertical layout; division uses a long-division bracket. Reveal worked steps when you need help. Correct answers earn 10 points and add to your streak; a wrong answer gently resets the streak and lets you retry. A solved question awards points only once. Changing or skipping questions does not award points. Score and best streak are saved only in this browser when storage is available; current streak resets on reload.

## Install / offline
Host these files on any static HTTPS site, retaining their relative paths. Visit once online to cache the app. On supported desktop/Android browsers, use the browser install option or the Install app button when available. On iPhone/iPad, open in Safari, Share → Add to Home Screen. Offline play works after a successful first load and service-worker installation. Installation UI varies by browser. No server/backend or shared leaderboard is included.

## Files
- index.html — accessible responsive UI
- style.css — local styling (no remote fonts)
- app.js — generation, checking, worked steps, local progress, install handling
- manifest.webmanifest — install metadata
- sw.js — offline app-shell cache
- icons/ — 192px, 512px, and maskable PNG icons

For future asset changes, bump the cache version in sw.js. This project is separate from math-arcade; nothing there was changed. It has not been deployed or pushed to GitHub.
