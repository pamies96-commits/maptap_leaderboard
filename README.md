# MapTap Weekly Leaderboard

A simple weekly leaderboard for tracking MapTap scores among friends, hosted on GitHub Pages.

## Files

- `index.html` — the leaderboard (public)
- `admin.html` — score input page
- `scores.json` — the data file (edit this to add scores)

## Setup on GitHub Pages

1. Create a new GitHub repository (e.g. `maptap-scores`)
2. Upload all three files (`index.html`, `admin.html`, `scores.json`)
3. Go to **Settings → Pages**
4. Under "Branch", select `main` and click **Save**
5. Your leaderboard will be live at `https://YOUR_USERNAME.github.io/maptap-scores/`

## Adding scores

### Option A — Paste raw result (recommended)
1. Open `admin.html` on your phone or browser
2. Select the player
3. Paste the MapTap result text directly (e.g. `www.maptap.gg April 6\n94🏅 94🏅 100🎯 97🔥 80✨\nFinal score: 919`)
4. Click **Add score** — a JSON entry is generated
5. Copy it and paste into `scores.json` on GitHub

### Option B — Manual entry
1. Open `admin.html`
2. Fill in player, date, final score, and optionally the 5 round scores
3. Copy the generated JSON entry into `scores.json`

## scores.json format

```json
{
  "players": ["Pausi", "Nili", "Carre", "Pami"],
  "scores": [
    {
      "date": "2026-04-06",
      "player": "Pausi",
      "final_score": 919,
      "rounds": [94, 94, 100, 97, 80],
      "raw": "www.maptap.gg April 6\n94🏅 94🏅 100🎯 97🔥 80✨\nFinal score: 919"
    }
  ]
}
```

- `date` — ISO format `YYYY-MM-DD`
- `player` — must match a name in the `players` array
- `final_score` — the game's total
- `rounds` — array of 5 individual round scores (optional but recommended)
- `raw` — the original paste from the game (optional)

## Weekly reset

No action needed — the leaderboard automatically shows only the current Mon–Sun week. Previous weeks appear in the "Previous weeks" section below the table.
