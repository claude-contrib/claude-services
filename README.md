# Claude Services

A curated collection of MCP servers for Claude Code.

[![Plugins](https://github.com/claude-contrib/claude-services/actions/workflows/validate.yml/badge.svg)](https://github.com/claude-contrib/claude-services/actions/workflows/validate.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What are Services?

Services are MCP (Model Context Protocol) servers that provide additional tools Claude uses autonomously during a session. They differ from:

- **Skills** ([claude-skills](https://github.com/claude-contrib/claude-skills)) — slash commands you invoke intentionally
- **Extensions** ([claude-extensions](https://github.com/claude-contrib/claude-extensions)) — hooks and context rules that run passively

## Installation

Add the marketplace to your Claude Code settings (`~/.claude/settings.json`):

```json
{
  "extraKnownMarketplaces": {
    "claude-services": {
      "source": {
        "source": "github",
        "repo": "claude-contrib/claude-services"
      }
    }
  }
}
```

Then install a service:

```text
/plugin install <plugin-name>@claude-services
```

## Available Services

| Plugin | Description |
| --- | --- |
| [`thinking-mcp`](plugins/thinking-mcp/README.md) | Sequential thinking for structured problem analysis |
| [`filesystem-mcp`](plugins/filesystem-mcp/README.md) | File system operations |
| [`playwright-mcp`](plugins/playwright-mcp/README.md) | Browser automation |

## Contributing

1. Fork this repository
2. Create a plugin directory under `plugins/<your-plugin>/`
3. Add `.claude-plugin/plugin.json`, a `.mcp.json` server config, and a `README.md`
4. Register your plugin in `.claude-plugin/marketplace.json`
5. Open a pull request — CI validates the structure automatically

See [docs/](docs/) for plugin development guides.

## License

MIT
