# Bills & Subscriptions Tracker — PWA

A fully interactive, installable bill tracker. Add bills, add your own columns, pick icons, and everything is saved on-device automatically. No account, no server, no cost.

## Try it locally right now
Just open `index.html` in a browser — it works immediately.

## Install it as an app on your phone (free, ~2 minutes)
To get the "Add to Home Screen" install prompt, the files need to be served over `https://` (phones won't offer to install a page opened straight from a file). Easiest free ways to do that:

### Option 1 — Netlify Drop (fastest, no account needed for a quick test)
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page
3. You'll get a free `https://something.netlify.app` link instantly
4. Open that link on your phone in Chrome → menu → **Add to Home Screen**

### Option 2 — GitHub Pages (best for something you'll keep long-term, still free)
1. Create a free GitHub account if you don't have one
2. Create a new repository, upload all the files in this folder
3. Go to the repo's **Settings → Pages**, set source to the main branch
4. GitHub gives you a `https://yourname.github.io/reponame` link
5. Open it on your phone → **Add to Home Screen**

Either way: once installed, it opens full-screen with its own icon, works offline, and every bill you add stays saved on that device.

## What's in this folder
- `index.html` — the whole app (UI + logic)
- `manifest.json` — tells the phone this is an installable app (name, icon, colors)
- `service-worker.js` — lets it work offline after the first load
- `icons/` — app icons used on the home screen

## Notes
- Data is stored locally in the browser (`localStorage`) — it stays on that device only. Clearing browser data will clear it too.
- Want it in the actual Google Play Store instead of "Add to Home Screen"? See the `app-build-and-publish-guide.md` from earlier — this same folder is exactly what gets wrapped with Capacitor for that path.
