# Renerose & Carlo RSVP

Mobile-friendly RSVP page with three responses (Yes, No, Maybe). Submissions are saved to the Google Sheet `Renerose & Carlo Wedding RSVP Responses`.

## Google Apps Script setup

1. Open the Google Sheet linked in this project.
2. Choose **Extensions → Apps Script**.
3. Replace the editor content with `Code.gs`.
4. Select **Deploy → New deployment → Web app**.
5. Set **Execute as** to your account and **Who has access** to **Anyone**. This is required so guests can submit without signing in. The app writes only to the sheet ID already set in the script.
6. Deploy, authorize the script, and copy the Web App URL ending in `/exec`.

## GitHub Pages setup

1. Put `index.html` at the root of a public GitHub repository.
2. Replace `PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE` in `index.html` with the Web App URL.
3. In repository **Settings → Pages**, deploy from the `main` branch and `/ (root)`.
4. Send guests the published Pages URL. Their Yes/No/Maybe responses will appear in the Google Sheet.

The app collects only guest name, response, party size when attending, and an optional message. The Sheet itself should remain private; only the Apps Script Web App needs public access for submissions.
