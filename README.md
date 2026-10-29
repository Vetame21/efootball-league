# eFootball Elite League ⚽

A shared web app for running an eFootball league with friends: standings, fixtures, score predictions and friendlies, all on one page that everyone edits together.

> **Forked from [magotmantap/efootball-league](https://github.com/magotmantap/efootball-league).** The app was built by **magot**; this fork is my copy for following the league and learning from the code.

**Live site (original):** https://efootball-league-seven.vercel.app

## Features

| Tab | What it does |
|---|---|
| **Table** | League standings: played, W/D/L, goals, goal difference, points and recent form |
| **Fixtures** | Double round-robin schedule (home and away), one round per week; enter results and change dates |
| **Friendly** | Friendly matches outside the league that still adjust player ratings |
| **Predictions** | Win/draw/loss chances for each match, plus title odds from 1,500 simulated seasons |
| **Players** | Ratings, personal stats and head-to-head records |
| **Stats** | Season awards and league-wide numbers |
| **Log** | Activity history of every change |

## How it works

- **One shared season.** All league data is saved under a single key in an Upstash Redis store, so everyone who opens the site sees and edits the same league.
- **Prediction model.** Each player's rating sets their attack and defence strength. Expected goals start at 1.6 per match, with a 10% home advantage. After about 5 matches, real results count more than the starting rating.
- **Fixtures.** Generated with the round-robin "circle method"; with an odd number of players, one player gets a bye each round.

## Tech stack

React 19 · Vite 8 · Upstash Redis (REST) · Vercel

## Run it locally

```bash
npm install
npm run dev
```

Then open http://localhost:5173.

## Credits

Original app and all game logic by [magot](https://github.com/magotmantap).
