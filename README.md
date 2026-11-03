# Palmate for Claude

The Palmate plugin marketplace for Claude on the web, desktop and mobile. It holds one plugin, `palmate`, which
connects Claude to your Palmate account: Claude can read the projects Palmate opened for this connection (bot
conversations, statistics, change requests) and help you ask Palmate for changes as change requests, which
Palmate's team reviews.

## Add it to Claude

1. In claude.ai or the Claude desktop app, open **Customize > Plugins > Add > Add marketplace** and enter
   `plmrtch/palmate-claude-plugin`. Turn on **Sync automatically** so new versions reach you without any action.
2. Install the **palmate** plugin.
3. On the plugin's **Connectors** tab, connect the Palmate connector and approve the connection on the Palmate page
   that opens (a second factor is required). No client ID is needed.

Your Palmate account must be an admin of a project Palmate opened for Claude; ask Palmate support to open yours.

## What it sends

Claude calls the Palmate connector at `https://api.palmate.ai/api/palmate-mcp/mcp/` with your own account: it reads
the data of the projects open to it and creates change requests you confirm. The plugin stores nothing itself. How
Claude should work with Palmate is served by the connector, so improvements reach you without a plugin update.

For Claude Code and direct project editing, use the Palmate CLI plugin in `plmrtch/palmate-plugins` instead.
