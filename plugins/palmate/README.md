# Palmate for Claude

Use Palmate from Claude on the web, desktop and mobile. The plugin connects Claude to your Palmate account so it can
read your chatbot projects (bot conversations, statistics, change requests), run your WhatsApp templates and
campaigns, and help you ask Palmate for changes as change requests, which Palmate's team reviews.

## Install

1. In claude.ai or the Claude desktop app, open **Customize > Plugins > Add > Add marketplace** and enter
   `plmrtch/palmate-assistant-plugin`. Turn on **Sync automatically** so new versions reach you without any action.
2. Install the **palmate** plugin.
3. On the plugin's **Connectors** tab, connect the Palmate connector and approve the connection on the Palmate page
   that opens (a second factor is required). No client ID is needed.

## What it contains

- The Palmate connector (`https://api.palmate.ai/api/palmate-mcp/mcp/`).
- One skill and two commands (`/change-request`, `/request-status`). They only point Claude at the guides the Palmate
  connector serves, so improvements to how Claude works with Palmate reach you without updating this plugin.

## What you can ask

- "How many conversations did the bot have last week, and how many went to a live agent?"
- "Show me a few conversations where customers asked about returns."
- "Create a WhatsApp template for our winter sale and tell me when Meta approves it."
- "Send the approved campaign to the VIP segment tomorrow at 10:00."
- "Ask Palmate to make the bot answer shipping questions in a shorter way."
- "What is the status of the change request I opened yesterday?"

Claude asks for your explicit yes before anything that cannot be taken back: sending, scheduling or stopping a
campaign, editing or deleting a template, or retraining the bot.

## What it cannot do

It cannot edit a project directly or cancel running work; changes go through change requests. Team management and
reviews are done in the Palmate dashboard. Direct editing is done in Claude Code with the Palmate CLI (the separate
`palmate-agent` plugin); this plugin's connector is for Claude on the web, desktop and mobile.

## Requirements

A Palmate account that is an admin of the project. Projects are open to Claude and ChatGPT by default; Palmate
support can close one.

## Privacy and terms

Claude calls the connector with your own account and sees only the projects open to it; the plugin stores nothing
itself. See the [Palmate privacy policy](https://palmate.ai/privacy-policy) and the
[terms of use](https://palmate.ai/privacy-policy#terms-of-use).
