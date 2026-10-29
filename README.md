# ❄️ Winter Arc — 8-Week Workout Tracker

A tap-to-log gym tracker for your phone. No typing mid-set, no account, no server — it works offline and your data never leaves your device.

<!-- Add a screenshot: ![Winter Arc on a phone](docs/screenshot.png) -->

**Try it:** https://Jebershon.github.io/winter-arc-tracker/

## Features

- Tap a set → scroll-wheel picker for kg and reps (or seconds) with ± buttons. No keyboard needed between sets.
- "Same as last time" and "Same as previous set" one-tap fills.
- Last session shown on every exercise, PR badge when you beat your best weight.
- Exercises tick themselves off when every set is logged.
- Rest timer with beep and vibration (60 s – 3 min, +15 s, skip).
- Quick "how did it feel" tags plus optional notes.
- Stats: workouts done, day streak, weekly volume vs last week, and an 8-week overview grid.
- Installable to the home screen and works offline (PWA).
- Data stays on your device (localStorage). JSON backup/restore and CSV export.
- Mobile-first layout, dark mode follows your phone.

## The plan

| Day | Session | Focus |
| --- | --- | --- |
| Mon | Push | Chest · Shoulders · Triceps |
| Tue | Pull | Back · Rear delts · Biceps |
| Wed | Legs + Abs | Quads · Hamstrings · Glutes · Calves · Core |
| Thu | Recovery | Easy walking · Light cardio · Mobility |
| Fri | Upper Body | Chest · Back · Side delts |
| Sat | Legs + Arms | Legs · Biceps · Triceps |
| Sun | Rest | |

To change exercises, sets or rep ranges, edit the `plan` object near the top of the `<script>` in `index.html`.

## Publish on GitHub Pages

1. Create a public repo named `winter-arc-tracker`.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `.nojekyll`, `README.md` to the repo root (or push with git):

   ```bash
   git init
   git add .
   git commit -m "Winter Arc workout tracker"
   git branch -M main
   git remote add origin https://github.com/Jebershon/winter-arc-tracker.git
   git push -u origin main
   ```

3. Go to Settings → Pages → Source "Deploy from a branch" → Branch `main` / `(root)` → Save.
4. After a minute, open `https://Jebershon.github.io/winter-arc-tracker/`.

## Install on your phone

- **iPhone:** open the link in Safari → Share → Add to Home Screen.
- **Android:** open in Chrome → ⋮ menu → Install app / Add to Home screen.

## Run locally

Opening `index.html` directly works, but offline caching needs a local server:

```bash
npx http-server -c-1 .
```

```bash
python -m http.server 8000
```

## Your data

Everything is stored in this browser's localStorage, per site. Clearing site data erases it. Export a JSON backup before switching phones and restore it on the new one. Nothing is sent anywhere.

## Tech

A single HTML file with vanilla JS and CSS, no build step, no dependencies. Fonts come from Google Fonts (Outfit and Inter).

## License

MIT — add a LICENSE file with your name if you publish this.
