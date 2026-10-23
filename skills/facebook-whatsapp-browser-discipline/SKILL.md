# Facebook and WhatsApp browser discipline

## Reuse the existing tab, always

- Apply this section to every `browser.browse` task touching facebook.com, business.facebook.com (Business Suite), messenger.com, or web.whatsapp.com. A new tab on these sites triggers bot detection and kills the login session.

- Find the existing `browser.browse` window for the site first and continue it by passing its `task_id`.

- Never start a fresh browser task for these sites when a live one exists.

- Say so and wait for direction when no live task exists for the site, instead of opening a new one on your own.

- Confirm after the work in one line which existing tab was reused. Report a newly opened tab as a violation immediately.

## Verify the session before you act

- Check on entry that you are still logged in by confirming the page shows the account, not a login form or QR code.

- Stop when the session expired and ask the user to re-login in the live browser, then continue in the same tab after they hand control back.

- Never re-attempt the action in a new tab to work around a lost session. The new tab is what kills it.

## Handle the WhatsApp file-attach block

- Treat WhatsApp Web Attach > Document as permanently blocked. It opens a native OS file picker that automation cannot drive, and the upload tool returns target_blocked.

- Do not retry it. One attempt that hits target_blocked ends the attempt.

- Route the file through the user's phone instead. Keep the PDF at `~/workspace/`, tell the user it is ready in chat, and let them forward it to the group.

## Available connectors

- [Facebook CLI](/opt/hatch/connectors/facebook_cli/CONNECTOR.md) for scripted Facebook reads and approved publishes. Prefer it over the browser whenever it covers the need, since fewer browser sessions means fewer logouts.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Batch all Facebook or WhatsApp actions into one session in the one existing tab instead of opening and closing tasks across the day.

- Pause browser work on that site when a session dies twice in one day, and ask the user before trying again. Repeated attempts deepen the bot-detection lockout.
