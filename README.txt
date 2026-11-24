# SARL GLOBAL DATA — Offline Devis & Factures

## What is included
- Existing invoice/quote layout and document controls
- Local CSS and Font Awesome files (no design CDN dependencies)
- Offline app shell cache through a service worker
- Local autosave in the browser on each device
- Android and iPhone PWA manifest/icons

## Important
The first installation/opening must happen while connected to the internet if hosted online, so the browser can download and cache the app. After the first successful load, the app shell can open offline. Data is saved separately in each device/browser. There is no cloud sync.

## Test on Windows
1. Install/use Python 3 if needed.
2. Open this folder in File Explorer.
3. In the folder address bar, type `cmd` and press Enter.
4. Run: `python -m http.server 8000`
5. Open `http://localhost:8000` in Chrome or Edge.

## Install on Android
Host this folder on an HTTPS website (for example, GitHub Pages). Open the website in Chrome, then choose **Install app** or **Add to Home screen**. Open it once while online, then test airplane mode.

## Install on iPhone
Open the HTTPS website in Safari, tap **Share**, then **Add to Home Screen**. Open it once while online, then test airplane mode.

## Notes
- Service workers require HTTPS, except on localhost. Opening `index.html` directly with `file://` will show the page but will not enable PWA offline caching.
- Browser storage is local to the device and browser profile. Clearing browser/site data can erase saved invoice information.
