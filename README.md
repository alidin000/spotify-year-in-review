# Spotify Year in Review

A single-page personal Spotify listening dashboard using Spotify's Web API and Authorization Code with PKCE. It requires no backend and no client secret in the browser.

## Features
- Top artists and tracks across three time ranges
- Recently played tracks
- Playlists and liked songs
- Currently playing track
- Export returned data as JSON
- Responsive dark dashboard

## Deploy with GitHub Pages
1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/ (root)`, then save.
4. Wait for GitHub Pages to publish the site.

## Spotify setup
1. Create an app at https://developer.spotify.com/dashboard.
2. Copy its Client ID.
3. Add the published GitHub Pages URL as a Redirect URI in the Spotify app settings. The URI must exactly match the site URL, including trailing slash.
4. Open the site, paste the Client ID, select **Save Client ID**, then **Connect Spotify**.
5. Approve the requested access.

The site uses PKCE (a browser-safe OAuth authorization flow) and never asks for your Spotify password or client secret. Spotify requests are made directly from your browser.

## Privacy
- Client ID is saved in local storage.
- Access tokens are kept in session storage.
- Disconnect to clear the current token.
- No listening data is sent to a separate backend.

## Limitations
Spotify's API does not provide the official Wrapped report or a complete lifetime listening history. The time ranges are Spotify's top-item ranges, not exact calendar-year reports. API endpoints and access depend on Spotify's current developer policies and app eligibility.
