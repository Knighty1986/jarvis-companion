# JARVIS Personal AI Companion — first prototype

## What works now
- Responsive, dark, iPhone-friendly dashboard.
- Add, complete and delete tasks with priority and due dates.
- Add people to a personal check-in list.
- Save notes locally in this browser.
- Simple check-in message draft helper and copy button.
- Text commands and a voice button using browser speech recognition when available.
- Spoken responses using the device/browser's available voices, preferring `en-GB`.
- Export local data as JSON; clear local data.
- PWA manifest and service worker shell for install/offline caching when hosted over HTTPS.

## What does not work yet
- No real AI model is connected: command handling is a small set of local rules.
- No email, calendar, contacts-provider or social-media accounts are connected.
- No server-scheduled reminders or push notifications are implemented.
- No authentication, cloud sync or cross-device backup.
- Voice availability and the exact British voice depend on the iPhone/browser and installed voices.

## Run locally
Open `index.html` in a browser for a basic preview. Some PWA and microphone features require HTTPS or localhost. For full install testing, deploy the folder to an HTTPS static host.

## Add to iPhone Home Screen
1. Host the folder at an HTTPS URL.
2. Open that URL in Safari on iPhone.
3. Tap Share → Add to Home Screen.
4. Enable “Open as Web App” if shown, then tap Add.

## Recommended next architecture
- Front end: this PWA, later TypeScript/React if desired.
- Backend: small serverless API for OAuth callbacks, AI calls, scheduled jobs and push delivery.
- Data/auth: Supabase or Firebase free tier to start, with a private user account and row-level access rules.
- Integrations: Gmail/Google Calendar or Microsoft Graph via OAuth; contacts imported with consent; social networks connected individually according to their API rules.
- Voice: start with Web Speech API where supported; for natural real-time conversational voice, add a speech/AI provider through a backend. Keep API keys out of browser code.
- Safety: read-only integrations first, draft-only messaging, explicit confirmation before sending, posting, deleting or creating calendar events.

This is a starter prototype, not a production-ready secure service.
