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

The same repository is a Cursor plugin (`.cursor-plugin/plugin.json`, `mcp.json`, the same `cobrain` skill), listed on [cursor.directory](https://cursor.directory/plugins/cobrain). Step-by-step guide: https://cobrain.space/guides/connect-cursor. In Grok Bot add `https://cobrain.space/mcp` under Connect apps and sign in.

## Hermes Agent

The repository root is also an [Agent Plugins](https://agent-plugins.org) v1 package (`plugin.json`, `mcp.json`, the `cobrain` skill), listed in the Hermes plugin catalog:

```
hermes plugins install cobrain
```

Portable `mcp.json` cannot complete OAuth yet, so add the server once to `~/.hermes/config.yaml` and sign in:

```yaml
mcp_servers:
  cobrain:
    url: https://cobrain.space/mcp
    auth: oauth
    trust: untrusted
```

```
hermes mcp login cobrain
hermes mcp test cobrain
```

## Gemini CLI

```
gemini extensions install https://github.com/Overpress-Media/cobrain-plugin
```

Then run `/mcp auth cobrain` inside Gemini CLI and sign in. The extension loads the same guidance as the skill (`GEMINI.md`).

## Cline

In Cline open **MCP Servers → Configure → Configure MCP Servers** and add:

```json
{
  "mcpServers": {
    "cobrain": { "type": "streamableHttp", "url": "https://cobrain.space/mcp" }
  }
}
```

Save, then sign in when Cline opens the browser (OAuth, no API key; a free account is enough). Try: *search my brain for "project"*.

## Links

- Tools reference: https://cobrain.space/guides
- Privacy policy: https://cobrain.space/privacy
- Support: hi@cobrain.space
