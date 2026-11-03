# Palmate for Claude

Use Palmate from Claude on the web, desktop and mobile. The plugin connects Claude to your Palmate account so it can
read the projects Palmate opened for this connection (bot conversations, statistics, change requests) and help you
ask Palmate for changes as change requests, which Palmate's team reviews.

## What it contains

- The Palmate connector (`https://api.palmate.ai/api/palmate-mcp/mcp/`). Connect it from the plugin's Connectors tab
  and approve the connection on the Palmate page that opens; a second factor is required. No client ID is needed.
- One skill and two commands (`/change-request`, `/request-status`). They only point Claude at the guides the Palmate
  connector serves, so improvements to how Claude works with Palmate reach you without updating this plugin.

## What it cannot do

It cannot edit a project directly or cancel running work; changes go through change requests. Direct editing is done
in Claude Code with the Palmate CLI (the separate `palmate-agent` plugin).

## Requirements

A Palmate account that is an admin of a project Palmate opened for Claude. Ask Palmate support to open your project.
