# My Voice - Khaleesi's Communication App

PWA communication app. Works on any phone/tablet. No app store required.

## Features

- 5 categories: Feelings, Food & Drinks, Activities, Needs, How I am right now
- Big emoji card grid (2-3 columns phone, 4 on tablet)
- "Something else" free text fallback on every category
- Confirmation screen after every selection
- Local history with timestamps (localStorage, up to 500 entries)
- Export history as plain text for NDIS/school reports
- Offline capable via service worker
- Installable as PWA (Add to Home Screen)

## Deploy

Needs HTTPS to install as a PWA. Quickest options:

### Vercel (recommended)
```
cd khaleesi-app
npx vercel --prod
```

### Netlify drag-and-drop
Drag the folder into app.netlify.com.

### GitHub Pages
Push to a repo, enable Pages, done.

## After deploying

1. Open the URL on Khaleesi's phone in Safari (iOS) or Chrome (Android)
2. Tap Share > Add to Home Screen (iOS) or Install App (Android)
3. Done. Works offline after first load.

## Customising

All category data is in the `CATS` object in `index.html`.
App name is in `<title>`, `<meta name="apple-mobile-web-app-title">`, and `manifest.json`.

## Files

- `index.html` - entire app (no build step, no dependencies)
- `manifest.json` - PWA config
- `sw.js` - service worker (offline caching)
- `icon.svg` - app icon
