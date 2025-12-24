# Sylvara Plugin Marketplace

A Claude Code plugin marketplace for productivity and development tools.

## Available Plugins

### nixos
NixOS option search, package lookup, and configuration helpers powered by the [mcp-nixos](https://github.com/utensils/mcp-nixos) MCP server.

**Features:**
- NixOS option search and documentation
- Package lookup and information
- Configuration assistance
- Integration with Claude Code for NixOS development

### memory
Persistent memory across Claude Code sessions using the official [@modelcontextprotocol/server-memory](https://github.com/modelcontextprotocol/servers).

**Features:**
- Store information that persists across sessions
- Build a personal knowledge base
- Cross-project availability
- Searchable memories
- Local SQLite storage

## Installation

### Add the Marketplace

```bash
/plugin marketplace add SylvaraTheDev/Marketplace
```

Or if using a local clone:

```bash
/plugin marketplace add ~/git/sylvara/marketplace
```

### Install Plugins

Install individual plugins:

```bash
# NixOS tools
/plugin install nixos@sylvara

# Persistent memory
/plugin install memory@sylvara
```

### Verify Installation

```bash
/plugin list
```

## Usage

Once installed, Claude Code will have access to:

**NixOS Plugin:**
- Understanding NixOS configuration options
- Finding and evaluating packages
- Writing and maintaining Nix expressions
- Troubleshooting NixOS configurations

**Memory Plugin:**
- Storing personal preferences and facts
- Building a knowledge base over time
- Cross-session persistence
- Cross-project context

## Requirements

- Claude Code CLI
- Node.js and npm (for MCP servers)
- Python and uv (for NixOS plugin)

## Contributing

This marketplace is maintained by Sylvara. To add more plugins or suggest improvements, please open an issue or pull request.

## License

MIT
