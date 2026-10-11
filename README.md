# PL Extended Highlights

Premier League scores + NBC Sports extended highlights, with a watched tracker. Built to run on GitHub Pages and be saved to the iPhone Home Screen.

## Setup
1. Upload `index.html`, `manifest.json`, `icon-180.png`, `icon-192.png`, `icon-512.png` to a GitHub repo.
2. Repo **Settings → Pages** → Deploy from branch `main`, folder `/ (root)`.
3. Get a free YouTube API key: console.cloud.google.com → create a project → enable **YouTube Data API v3** → Credentials → Create API key. Restrict it to *HTTP referrers* `https://YOURNAME.github.io/*` and to the YouTube Data API.
4. Open the Pages URL in Safari → Share → **Add to Home Screen**.
5. Open the app → gear icon → paste the API key. It's stored only on your phone, not in the repo.

## How it works
- Scores: ESPN's public Premier League scoreboard (no key needed).
- Videos: reads the NBC Sports YouTube uploads list (1 quota unit per 50 videos, well within the free 10,000/day) and matches titles containing "Extended" to each fixture by team name.
- Refreshes every few minutes (every minute during live matches) and when you reopen the app. YouTube is only checked while a finished match is still missing its video.
- Watched marks are saved on the device.
