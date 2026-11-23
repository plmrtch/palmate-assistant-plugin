# Palmate for Claude and ChatGPT

The Palmate plugin marketplace for Claude on the web, desktop and mobile, and the same plugin for ChatGPT. It holds one plugin, `palmate`, which
connects Claude to your Palmate account: Claude can read the projects Palmate opened for this connection (bot
conversations, statistics, change requests) and help you ask Palmate for changes as change requests, which
Palmate's team reviews.

## Add it to Claude

1. In claude.ai or the Claude desktop app, open **Customize > Plugins > Add > Add marketplace** and enter
   `plmrtch/palmate-claude-plugin`. Turn on **Sync automatically** so new versions reach you without any action.
2. Install the **palmate** plugin.
3. On the plugin's **Connectors** tab, connect the Palmate connector and approve the connection on the Palmate page
   that opens (a second factor is required). No client ID is needed.

Your Palmate account must be an admin of the project. Projects are open to Claude and ChatGPT by default; Palmate
support can close one.

## Add it to ChatGPT

The same folder, `plugins/palmate`, is also a ChatGPT plugin: ChatGPT reads the root `plugin.json` and `mcp.json`
(Claude reads `.claude-plugin/plugin.json` and `.mcp.json`; the skill is shared, the two commands are Claude-only).

1. Add `plugins/palmate` as a personal plugin, or have a workspace admin publish it. Custom MCP servers need a paid
   plan: Business and Enterprise/Edu get every tool, Pro gets the read tools only (OpenAI's plan rules).
2. Connect the Palmate connector and approve the connection on the Palmate page that opens. No client ID is needed:
   ChatGPT identifies itself with its own client metadata document.

Keep the connector URL the same in `mcp.json` and `.mcp.json`.

## What it sends

Claude (or ChatGPT) calls the Palmate connector at `https://api.palmate.ai/api/palmate-mcp/mcp/` with your own account: it reads
the data of the projects open to it and makes the changes you confirm (change requests, WhatsApp templates
and campaigns). The plugin stores nothing itself. How
Claude should work with Palmate is served by the connector, so improvements reach you without a plugin update.

For Claude Code and direct project editing, use the Palmate CLI plugin in `plmrtch/palmate-plugins` instead.
