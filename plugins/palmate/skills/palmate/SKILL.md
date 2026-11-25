---
name: palmate
description: Use whenever the user mentions Palmate or their chatbot, live support or WhatsApp business messaging - reading or analysing bot conversations, statistics and reports; WhatsApp templates, contact lists, segments and campaigns (create, schedule, send, stop, track); asking for a change to the bot (a change request) or reporting a platform problem (a support request); or following up on any of these.
---

# Palmate

Palmate's instructions are served by the Palmate connector and change as Palmate improves them; they are not in this
file. Read them from the connector every time instead of relying on what you remember.

1. At the start of a conversation about a Palmate project, call `get_palmate_guide` with topic `overview` and follow it.
2. Its answer lists the other guides (`topics`). Before a task one of them covers (a change request, a follow-up,
   conversations and statistics, a WhatsApp template or campaign, a support request), read that guide first.
3. Call Palmate tools one at a time, never several at once. For numbers and trends use the statistics figures
   (`list_statistics_pages`, `run_statistics_figure`), not conversation lists; read conversations only as a few
   examples. If a tool says Palmate is busy or the query is too heavy, stop and tell the user; do not retry.
4. Never send, schedule or stop a campaign, or edit or delete a template, without the user's explicit yes in this
   conversation.
5. If the Palmate tools are not available, the connector is not connected: ask the user to connect the Palmate
   connector from this plugin's settings (in Claude, the plugin's Connectors tab). Do not answer from guesswork.
