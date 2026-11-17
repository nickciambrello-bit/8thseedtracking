# JandO League 8th Seed Race

A one-page tracker and playoff simulator for the JandO League on Sleeper.

League rule: seeds 1-7 go by record (points-for breaks ties). The 8th seed goes to whoever has the most total points-for among everyone else (seeds 8-12).

## What's in it

- **The Race**: who holds seed 8 right now, the points-for gap for every team chasing it, seed-8 and top-7 odds, a week-by-week grid of where each team stood, and full standings.
- **Simulator**: 10,000 Monte Carlo runs of the rest of the regular season. Tap a team to make them win a game, or type a score to lock in exact points. You get playoff odds, seed distribution, and the games that swing a chosen team's odds the most. Picks are saved in your browser.
- **Paths to 8th**: for every team, a plain-language list of what has to happen for them to take seed 8: the weekly score they need, which rivals they have to outscore (or need to climb into the top 7), and which game results help most. It uses the same simulations, including any picks you've made.

It pulls live data from the public Sleeper API every time the page opens, so it updates itself each week. No server, no API key.

## Put it on GitHub Pages

1. Create a new public repo on GitHub (for example `jando-8th-seed`).
2. Upload `index.html`, `snapshot.js` and this README to the repo root (Add file > Upload files).
3. Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
4. After a minute the site is live at `https://<your-username>.github.io/jando-8th-seed/`.

## Settings

- Different league: open the page with `?league=<sleeper league id>`, or change `DEFAULT_LEAGUE_ID` near the top of the script in `index.html`.
- If your league guarantees division winners a top-7 seed, tick the checkbox on the page.
- `snapshot.js` is a saved copy of the league from Nov 17, 2026 that the page falls back to only if Sleeper can't be reached. You can delete it.

Data from the public Sleeper API. Not affiliated with Sleeper.
