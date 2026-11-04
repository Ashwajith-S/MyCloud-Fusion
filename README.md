# MyCloud Fusion v2

A static GitHub Pages dashboard that can connect up to three Google accounts using Google Identity Services and list Google Drive file metadata.

## Google Cloud setup
1. In Google Cloud Console, create/select a project and enable **Google Drive API**.
2. Configure the OAuth consent screen. For a personal app in Testing mode, add each Google account you will use as a test user. Follow Google's current account/age requirements; if you cannot create a Cloud project, ask a parent/guardian to help with setup.
3. Create an OAuth Client ID of type **Web application**.
4. Add this Authorized JavaScript origin: `https://ashwajith-s.github.io`
5. Do not create or place a client secret in this static website. The app uses the browser token flow.
6. Open MyCloud on your phone, choose **Set up Google connection**, and paste the Web Client ID.

## Permissions and limitations
- Requests `openid email profile` and `https://www.googleapis.com/auth/drive.metadata.readonly`.
- Lists file names, MIME types, modified dates and Drive web links. It does not download file contents, upload, edit, or delete files.
- OAuth access tokens are held in JavaScript memory only, not localStorage or GitHub. Closing/reloading the page clears connected sessions; reconnect to use it again.
- Up to three distinct Google accounts can be connected in one browser session. Google account quotas remain separate.
- GitHub Pages is public static hosting. Never commit private files, OAuth tokens, passwords, or client secrets.
