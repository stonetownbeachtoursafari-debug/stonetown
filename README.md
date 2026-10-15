# Stone Town Beach Tours — WhatsApp Cloud API server

This is a deploy-ready Node.js server for the live integration.

## What it does
- Receives WhatsApp Cloud API webhook messages.
- Detects tour, people count, dates and times.
- Understands couple language such as “my boyfriend”, “my girlfriend”, “couple”, “the two of us”.
- Detects the customer's country code from their WhatsApp phone number.
- Replies with the exact configured price for 1 or 2 people and 4–8 people.
- Keeps 3-person price unconfigured until the owner supplies it.
- Creates pending bookings and supports Confirm/Cancel from the admin dashboard.
- Stores bookings/messages in `data.json`.

## Live setup
1. Install Node.js 18+.
2. Run `npm install`.
3. Copy `.env.example` to `.env` and fill in the Meta values.
4. Run `npm start`.
5. Deploy behind HTTPS on a server/hosting provider.
6. In Meta's WhatsApp configuration, set the webhook callback URL to `https://YOUR-DOMAIN/webhook` and the verify token to the same `VERIFY_TOKEN`.
7. Subscribe the app to WhatsApp message webhooks.
8. Open `https://YOUR-DOMAIN/` and use the `ADMIN_KEY` to view the dashboard.

Do not put access tokens in browser code or share them in chat. The Cloud API credentials must be stored as server environment variables.
