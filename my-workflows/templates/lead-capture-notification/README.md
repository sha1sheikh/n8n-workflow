# Template: Lead Capture & Notification

A ready-to-sell automation. When a lead submits a form, it validates the email,
logs the lead to a Google Sheet, pings a Slack channel, and returns a friendly
confirmation — instantly, with no manual work.

This is one of the most in-demand automations for small businesses, agencies,
coaches, and service providers. Easy to explain, easy to demo, obvious value.

## Flow

```
Lead Form Webhook (POST /lead-capture)
        │
   Normalize Fields  (name, email, message, receivedAt)
        │
    Valid Email?  ──no──►  Respond Error (400)
        │ yes
        ├──►  Log to Google Sheet
        └──►  Notify Slack
                   │
              Respond Success (200 + thank-you message)
```

## What the client needs to set up (their own credentials)

The workflow ships **without secrets** — the client (or you, on their instance)
plugs these in:

1. **Google Sheets** credential (OAuth2) — then replace `REPLACE_WITH_GOOGLE_SHEET_ID`
   with their sheet ID, and make sure the sheet has columns:
   `name | email | message | receivedAt`.
2. **Slack** credential (OAuth2) — then replace `REPLACE_WITH_SLACK_CHANNEL_ID`
   with the target channel ID.
3. Point their website form / landing page at the webhook URL n8n gives you
   (activate the workflow to get the production URL).

## Import it

In the client's n8n: **Workflows → Import from File → select `workflow.json`**.
Then open each node flagged with a credential and connect their account.

## Deploy it with Claude Code (faster)

From a Claude Code session with n8n-mcp connected to a running n8n:

> "Validate `my-workflows/templates/lead-capture-notification/workflow.json`
>  and deploy it to n8n."

Claude will run `validate_workflow`, fix anything the validator flags, then
`n8n_create_workflow` to push it live. Always validate before deploying.

## Customization ideas (upsells)

- Swap Google Sheets for **HubSpot / Airtable / Notion / a CRM**.
- Add an **auto-reply email** (Gmail / SMTP node) to the lead.
- Add **lead scoring** or spam filtering before notifying.
- Route hot leads to a **different Slack channel** or send an SMS (Twilio).

Each of these is a natural add-on you can charge extra for.

## Suggested price

- As a **done-for-you setup** on the client's instance: see `../../PRICING.md`
  (fits the "Starter Automation" tier).
- As a **downloadable template product**: a low one-time price; the money is in
  the customization and the retainer, not the raw JSON.
