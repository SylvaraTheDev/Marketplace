# Sylvara NixOS Plugin Marketplace

A Claude Code plugin marketplace for NixOS development and configuration tools.

## Available Plugins

### nixos
NixOS option search, package lookup, and configuration helpers powered by the [mcp-nixos](https://github.com/utensils/mcp-nixos) MCP server.

**Features:**
- NixOS option search and documentation
- Package lookup and information
- Configuration assistance
- Integration with Claude Code for NixOS development

## Installation

### Add the Marketplace

```bash
/plugin marketplace add sylvara/marketplace
```

Or if using a local clone:

```bash
/plugin marketplace add ~/git/sylvara/marketplace
```

### Install the NixOS Plugin

```bash
/plugin install nixos@sylvara-nixos
```

### Verify Installation

```bash
/plugin list
```

## Usage

Once installed, Claude Code will have access to NixOS-specific tools and can help you with:
- Understanding NixOS configuration options
- Finding and evaluating packages
- Writing and maintaining Nix expressions
- Troubleshooting NixOS configurations

## Requirements

- Claude Code CLI
- Node.js and npm (for the MCP server via npx)

## Contributing

This marketplace is maintained by Sylvara. To add more plugins or suggest improvements, please open an issue or pull request.

## License

MIT
