# Debtors Management System — Free Offline Android Installable App

This is a Progressive Web App (PWA) edition of the free local Debtors Management System. It has no subscription, paid backend, account, or cloud dependency.

## Files
- `index.html` — application
- `manifest.webmanifest` — Android install metadata
- `sw.js` — offline application cache
- `icons/` — app icons
- `README.txt` — this guide

## Important: one-time installation setup
Android requires a secure website (HTTPS) or localhost to install a PWA and register its offline service worker. A file opened directly from Downloads (`file://`) still works for local testing, but **Install app** and the offline app-shell cache are not available from a file URL.

To install on Android without paying for hosting:
1. Publish these files to a free static HTTPS host, for example a free GitHub Pages site. This is a one-time setup and does not require a paid subscription.
2. Open the HTTPS address in Chrome on your Android phone while online.
3. Tap **Install app** if it appears, or Chrome menu → **Install app** / **Add to Home screen**.
4. Open the installed app once while online so its app files are cached. Then it can reopen offline.
5. The debtor records themselves are stored locally on that phone in the browser's IndexedDB. Keep using Backup & restore to download JSON backups.

## Offline and privacy notes
- No records are uploaded to a server by this application.
- No synchronisation between devices.
- Do not clear Chrome site data; doing so can delete the local records.
- Back up regularly and store the backup somewhere safe.
- The app does not have a built-in password lock. Protect your phone with its screen lock.
- This is an installable PWA, not a signed APK file from the Play Store.

## If you do not want to publish it anywhere
You can still extract the ZIP and open `index.html` directly in Chrome for local use, but browser restrictions mean it will not install as a proper PWA from the file.
