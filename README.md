# Cobrain plugin

One memory for all your AIs. [Cobrain](https://cobrain.space) keeps your notes, decisions and context as Markdown in a brain that Claude, ChatGPT, Codex and any MCP client read and write.

This plugin adds:

- **the Cobrain connector** (`https://cobrain.space/mcp`, remote MCP with OAuth sign-in);
- **the `cobrain` skill**, which teaches the AI when to load context and how to save to the brain without overwriting it.

## Install

In Claude Code:

```
/plugin marketplace add Overpress-Media/cobrain-plugin
/plugin install cobrain@cobrain
```

On first use the client opens the Cobrain sign-in page. A free account is enough.

## Cursor and Grok Bot

The same repository is a Cursor plugin (`.cursor-plugin/plugin.json`, `mcp.json`, the same `cobrain` skill). Until it is listed in the marketplace, add the connector by hand: in Settings > MCP (Cursor) or Connect apps (Grok Bot) add `https://cobrain.space/mcp` and sign in.

## Links

- Tools reference: https://cobrain.space/guides
- Privacy policy: https://cobrain.space/privacy
- Support: hi@cobrain.space
