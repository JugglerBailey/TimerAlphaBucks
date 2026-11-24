# AlphaBucks

A party timer for one phone passed around a group: a random letter, a list of topics, 30 seconds to get through them all.

Plain HTML/CSS/JS with no build step: `index.html`, `manifest.json`, `sw.js` and the icons.

## How to play
- **Start**, then **Correct** to finish a topic or **Skip** to send it to the back of the list.
- Win by clearing every topic before the timer runs out.
- **Hold the topic area for 3 seconds** to open settings. This pauses a running round.

## Run locally
```
python3 -m http.server 8000
```
Then open http://localhost:8000.

## Host it (HTTPS is needed to install it)
**GitHub Pages:** repo Settings → Pages → Source: "Deploy from a branch" → pick the branch and `/ (root)`.
**Netlify:** drag this folder onto https://app.netlify.com/drop.

When you change any file, bump `VERSION` in `sw.js` so installed copies update.

## iPhone notes
- Open the link in Safari → Share → **Add to Home Screen**.
- The home-screen app stores its settings separately from Safari. Set up your topics in the home-screen app.
- The time's-up beep uses Web Audio, which iOS mutes when the **silent switch** is on. The red flash still shows.
- Keeping the screen awake needs iOS 16.4+ (iOS 18.4+ for the home-screen app).
