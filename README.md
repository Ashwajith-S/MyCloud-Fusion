# MyCloud Fusion — preview app

This is a responsive installable PWA prototype based on the approved light Liquid Glass design.

## Run it
- Unzip the folder.
- Open `index.html` in a modern browser for a local preview.
- For PWA installation/offline caching, host it on HTTPS (or run a local development server).

## Current features
- Responsive curved Liquid Glass dashboard.
- Home, Files, Search and Profile navigation.
- Connected-account dashboard layout and storage summary.
- Setup dialog for an OAuth client ID (saved locally in this browser).
- PWA manifest and basic service worker.

## Important: what is not connected yet
This is a front-end prototype. It does **not** yet sign in to Google, read Drive files, upload or download cloud files. The account cards are empty until a real provider integration is implemented. Do not enter your Google password into this app.

To enable real Google Drive access, the next development step is to configure a Google Cloud project, OAuth consent screen and Drive API with the minimum required scopes, then implement Google's official OAuth flow and Drive API calls. Each account must authorize separately. Keep tokens secure and follow Google's API policies; this app is designed as a unified file manager, not to evade storage quotas.

## Cost
The app source is free. Hosting may have free options, but no provider can guarantee free hosting forever. Avoid enabling paid billing unless you explicitly choose it.
