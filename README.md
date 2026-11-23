# JandO League 8th Seed Race

A one-page tracker and playoff simulator for the JandO League on Sleeper.

League rule: seeds 1-7 go by record (points-for breaks ties). The 8th seed goes to whoever has the most total points-for among everyone else (seeds 8-12).

## What's in it

- **The Race**: who holds seed 8 right now, the points-for gap for every team chasing it, seed-8 and top-7 odds, a week-by-week grid of where each team stood, and full standings.
- **Simulator**: 10,000 Monte Carlo runs of the rest of the regular season. Tap a team to make them win a game, or type a score to lock in exact points. You get playoff odds, seed distribution, and the games that swing a chosen team's odds the most. Picks are saved in your browser.
- **Paths to 8th**: a scenario board (one row per contender, one column per remaining week: opponent, the result that helps, typical score needed), a grid of playoff odds for every possible final record, and a card per team with its week-by-week path to seed 8 plus the other game results that help most. It uses the same simulations, including any picks you've made.
- **Schedule Swap**: pick two teams and trade their schedules for the whole season. Everyone keeps the points they actually scored; only opponents change. Shows both teams' new records, a week-by-week comparison with flipped results outlined, league standings and playoff odds real vs swapped, and one team's record under every other team's schedule. A checkbox applies the swap to the other tabs too.
- **Playoff Formats**: toggle between six seeding formats (8th by points, 7th & 8th by points, all 8 by points, 8th by median record, 7th & 8th by median record, all 8 by median record) to see the seeding, how each team got in, and playoff odds under each, plus every format side by side.

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
