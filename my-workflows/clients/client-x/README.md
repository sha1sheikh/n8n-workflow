# Client: Client X

## Contact
- Name / company: Client X (placeholder — update when known)
- Email:
- n8n instance: local (http://localhost:5678)

## What they wanted
- Problem being solved: capture leads from a web form, log them, and get notified
- Trigger: POST to the `lead-capture` webhook
- Actions: validate email, log to Google Sheet, notify Slack, respond to submitter
- Systems involved: Google Sheets, Slack

## What I delivered
- Template(s) used: `templates/lead-capture-notification`
- Customizations made: renamed to "Client X - Lead Capture & Notification"; Google Sheet ID and Slack channel ID left as placeholders (`REPLACE_WITH_GOOGLE_SHEET_ID`, `REPLACE_WITH_SLACK_CHANNEL_ID`) pending client's actual values
- Date delivered:
- Webhook / production URLs (no secrets — references only): `POST /lead-capture` (production URL available once activated in n8n)

## Credentials the client provided (names only — NEVER store secrets here)
- [ ] Google Sheets (OAuth2)
- [ ] Slack (OAuth2)

## Commercials
- Package / tier:
- Build fee:
- Monthly retainer:
- Renewal / review date:

## Notes & quirks
- Sheet ID and Slack channel ID still need to be filled in before the workflow is fully functional — currently deployed with placeholder values.
