---
name: palmate
description: Use whenever the user asks about their Palmate projects, chatbot conversations, live support or statistics, wants something in their Palmate bot changed, fixed, added or reported on, or asks about a change request they opened.
---

# Palmate

Palmate's instructions are served by the Palmate connector and change as Palmate improves them; they are not in this
file. Read them from the connector every time instead of relying on what you remember.

1. At the start of a conversation about a Palmate project, call `get_palmate_guide` with topic `overview` and follow it.
2. Before helping the user ask for any change, call `get_palmate_guide` with topic `change_request`.
3. When the user asks about a request they already opened, call `get_palmate_guide` with topic `follow_up`.
4. If the Palmate tools are not available, the connector is not connected: ask the user to connect the Palmate
   connector from this plugin's settings (in Claude, the plugin's Connectors tab). Do not answer from guesswork.
