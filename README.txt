# KAIROS V — The Elderglen Saga (Android-installable PWA)

## What this package contains
- `index.html`: the playable game
- `manifest.webmanifest`: install metadata
- `sw.js`: offline cache/service worker
- icons: SVG and PNG app icons

## Install on Android
A PWA must be served from HTTPS (or localhost); opening `index.html` directly from Files will not show Install App.

### Quick publish using GitHub Pages
1. Create a GitHub repository and upload **all files in this folder** to the repository root.
2. In the repository, open **Settings → Pages**.
3. Select deploy from the `main` branch and `/ (root)`, then Save.
4. Open the published HTTPS URL in Chrome on Android.
5. Tap Chrome's ⋮ menu → **Install app** (or **Add to Home screen**) → Install.
6. Launch KAIROS from the new home-screen icon. Open it online once before using offline so the service worker can cache it.

## Progress / privacy
Game progress is stored locally in the browser's localStorage. It does not automatically sync between devices. Use Export Save inside the game for backups. Clearing browser/site data can erase local progress.

## Important limitations
- This is an installable web app, not a signed native Android APK.
- Browser notifications, alarms, and background reminders are not included.
- The app shell is cached for offline launch after the first successful online visit; browser storage policies can still clear cached data.
