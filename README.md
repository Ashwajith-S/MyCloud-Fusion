# MyCloud Fusion v2

A personal, browser-based dashboard for connecting multiple Google Drive accounts.

## Features
- Add as many account slots as practical using **＋ Add account**.
- Connect separate Google accounts with Google Identity Services.
- View Drive file names and basic metadata with read-only access.
- Switch between accounts, load more results, refresh, and disconnect.
- OAuth access tokens are held in browser memory for the current session and are not committed to this repository.

## Important limitations
- Account slots do not combine Google storage quotas. Each account remains subject to Google's storage, API, OAuth, and usage limits.
- The app currently lists file metadata only; it does not upload, edit, or delete files.
- Reconnecting after a page reload may be required because access tokens are not persisted.
- GitHub Pages is public hosting. Do not commit private files, passwords, OAuth client secrets, or access tokens. A browser OAuth Client ID is not a client secret.

## Google setup
1. Create a Google Cloud project and enable the Google Drive API.
2. Configure the OAuth consent screen / Google Auth Platform.
3. Create an OAuth client of type **Web application**.
4. Add your GitHub Pages origin as an authorized JavaScript origin: `https://ashwajith-s.github.io`.
5. Paste the Web Client ID into the app using **Set up Google connection**.
6. Add the required test users if the OAuth app is in testing mode.

The app requests `drive.metadata.readonly` plus basic profile/email scopes.
