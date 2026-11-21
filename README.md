# Movai v0.3

A mobile-first TMDB discovery and personal media companion.

## Features
- Trending, popular movies and TV, multi-search, title details and TV season/episode metadata via TMDB.
- India streaming-provider availability shown when TMDB has data (availability can change; confirm with the service).
- Direct playback for media URLs supported by the browser, plus optional HLS.js playback.
- Optional HTTPS iframe for an embed provider that you own or are authorized to use.
- Optional VTT subtitles for direct video playback.
- Direct-download handoff only for URLs the user is authorized to download; hosts may prevent downloading.
- Capacitor configuration for Android packaging.

## TMDB setup
1. Create a TMDB API key / Read Access Token at https://www.themoviedb.org/settings/api.
2. Open Movai, go to Settings, and paste the Read Access Token. It is stored in localStorage on that device.
3. TMDB metadata and watch-provider availability require network access.

## Run locally
This is a static web app. Serve the `cinewave` folder with any static HTTP server, or open `index.html` in a modern browser (some browser features may require HTTP/HTTPS).

## Android packaging
Install Node.js and Android Studio, then from this folder:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

Build a debug APK in Android Studio via Build > Build Bundle(s) / APK(s) > Build APK(s). A signed release APK requires your own signing keystore.

## Important limitations
- TMDB supplies metadata and provider availability, not video files.
- Movai does not scrape, bypass DRM, defeat access controls, or provide unauthorized media sources.
- Only use official services or direct/embed sources you own or are licensed to access. Download availability depends on the host's permissions and technical controls.
- Third-party embed URLs may refuse framing or be unavailable in WebView.

## Attribution
This product uses the TMDB API but is not endorsed or certified by TMDB. Follow TMDB's current attribution and branding requirements before public release.
