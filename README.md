# Reel FC

Premier League and Champions League scores + extended highlights (NBC Sports for PL, CBS Sports Golazo for UCL), with a watched tracker. Runs on GitHub Pages and is saved to the iPhone/iPad Home Screen.

## Files
| File | What it is | Replace on updates? |
|---|---|---|
| index.html | The app | Yes |
| version.json | Current version + "what's new" notes | Yes |
| manifest.json | App name, colours, icons for the Home Screen | Only when changed |
| icon-180/192/512.png | Home Screen icons | Only when changed |
| config.js | Your YouTube API key | **No — set once, keep yours** |

## Setup
1. Upload all files to the repo root; Settings → Pages → deploy from `main`, root folder.
2. Edit `config.js` on GitHub and paste your YouTube Data API key between the quotes.
   Restrict the key in Google Cloud: Websites → `https://ashroll-jpg.github.io/*`, API → YouTube Data API v3 only.
3. Open the site in Safari → Share → Add to Home Screen.
4. Optional sync: Me tab → Sync across devices → paste a GitHub token with only the `gist` scope (same token on each device).

## How it works
- Scores, tables and the UCL knockout bracket: ESPN's public Premier League and Champions League feeds.
- Videos: NBC Sports (PL) and CBS Sports Golazo (UCL) YouTube uploads, matched to fixtures by team names; 6+ minutes counts as extended.
- Matches are grouped into Weekend (Fri–Mon) and Midweek (Tue–Thu) blocks.
- Updates: the app checks `version.json` and shows a pop-up when a newer version is live.
