# Memory Plugin for Claude Code

Provides persistent memory across Claude Code sessions using the official [@modelcontextprotocol/server-memory](https://github.com/modelcontextprotocol/servers) MCP server.

## Features

- **Persistent Storage**: Remember information across sessions
- **Knowledge Base**: Build a personal knowledge base over time
- **Cross-Project**: Available in all projects, not just one
- **Searchable**: Find stored memories easily
- **SQLite Backend**: Reliable local storage

## What You Can Store

- Personal preferences and coding style
- Frequently used commands or patterns
- Project relationships and context
- Facts about your workflow
- Anything you want Claude to remember

## Installation

### Via Marketplace

```bash
# Add the Sylvara marketplace
/plugin marketplace add SylvaraTheDev/Marketplace

# Install the plugin
/plugin install memory@sylvara
```

### Standalone

```bash
claude mcp add --transport stdio memory -- npx -y @modelcontextprotocol/server-memory
```

## Usage

Once installed, you can ask Claude to remember things:

### Store Information
- "Remember that I prefer TypeScript over JavaScript"
- "Store this pattern for future reference"
- "Remember my git email is wing@elyria.dev"

### Retrieve Information
- "What do you know about my coding preferences?"
- "Recall what you know about my workflow"
- "What email do I use for git commits?"

### Manage Memories
- "List all stored memories"
- "Delete the memory about X"
- "Update my preference for Y"

## How It Works

The Memory MCP server stores information in a local SQLite database. This data persists across:
- Different Claude Code sessions
- Different projects
- System restarts

The memories are stored locally on your machine and are not shared with anyone.

## Difference from Serena Memory

| Feature | Serena Memory | Memory Plugin |
|---------|---------------|---------------|
| **Scope** | Project-specific | Global, all projects |
| **Purpose** | Code patterns, project structure | Personal preferences, facts |
| **Location** | `.serena/` in project | Centralized database |
| **Access** | When project activated | Always available |

Use both together for the best experience!

## Requirements

- Claude Code CLI
- Node.js and npm (for running the MCP server)

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

### Clear all memories

If you want to start fresh, you can delete the SQLite database (location varies by OS).

## Credits

This plugin wraps the official [@modelcontextprotocol/server-memory](https://github.com/modelcontextprotocol/servers) from the Model Context Protocol project.

## License

MIT
