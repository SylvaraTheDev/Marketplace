# NixOS Plugin for Claude Code

Provides NixOS-specific tools and helpers through the [mcp-nixos](https://github.com/utensils/mcp-nixos) MCP server.

## Features

- **Option Search**: Find and understand NixOS configuration options
- **Package Lookup**: Search and get information about packages in nixpkgs
- **Configuration Assistance**: Help with writing and maintaining Nix expressions
- **Integration**: Seamless integration with Claude Code for NixOS development

## Installation

### Via Marketplace

```bash
# Add the Sylvara marketplace
/plugin marketplace add sylvara/marketplace

# Install the plugin
/plugin install nixos@sylvara
```

### Standalone

```bash
claude mcp add --transport stdio nixos -- uvx mcp-nixos
```

## Usage

Once installed, you can ask Claude Code questions like:

- "What NixOS options are available for configuring networking?"
- "Find packages related to Wayland compositors"
- "Help me understand this Nix expression"
- "What's the proper way to configure systemd services in NixOS?"

Claude will use the NixOS MCP server to provide accurate, up-to-date information from the NixOS ecosystem.

## Requirements

- Claude Code CLI
- Python and uv (for running the MCP server via uvx)
- Internet connection (for downloading the MCP server on first use)

## Troubleshooting

### Plugin not loading

Check the plugin status:
```bash
/plugin list
```

### MCP server errors

View errors in the plugin manager:
```bash
/plugin
# Navigate to the Errors tab
```

## Credits

This plugin wraps the [mcp-nixos](https://github.com/utensils/mcp-nixos) MCP server by @tychoish.

## License

MIT
