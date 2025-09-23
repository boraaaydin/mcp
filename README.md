# MCP Server Definitions for Claude Code

Loading all MCP servers simultaneously in Claude Code consumes unnecessary context window space. Claude Code allows you to load a single MCP server before any session.
This repository stores some of the most commonly used MCP servers so you can use them with ease.

Windows

```cmd
# Option 1: Temporary (current session only)
set REF_API_KEY=your_ref_api_key_here
claude --mcp-config \{path-to-file}\{mcp-server}.json

# Option 2: Permanent (system-wide)
setx REF_API_KEY "your_ref_api_key_here"
# Note: Close and reopen terminal after setx, then run:
claude --mcp-config \{path-to-file}\{mcp-server}.json
```

Mac - use with aliases

```zsh
# For zsh users
echo "source $(pwd)/.mcp-aliases" >> ~/.zshrc
source ~/.zshrc

# For bash users
echo "source $(pwd)/.mcp-aliases" >> ~/.bashrc
source ~/.bashrc
```

## MCP Servers

| Server | Alias | Category | Description |
|--------|-------|----------|-------------|
| Playwright | `claude-playwright` | Testing | Browser automation and web testing capabilities |
| BrowserMCP | `claude-browsermcp` | Testing | Browser automation and web scraping capabilities |
| Context7 | `claude-context7` | Documentation | Upstash's context management service for storing and retrieving contextual data |
| Ref | `claude-ref` | Documentation | HTTP-based MCP server for API reference and tools |
| Sequential Thinking | `claude-sthink` | Thinking | MCP server that provides sequential thinking capabilities for enhanced reasoning |
| GitHub | `claude-github` | Development | GitHub integration for repository management and code collaboration |
| Supabase | `claude-supabase` | Database | PostgreSQL database and backend-as-a-service integration |

## Contributing

Feel free to contribute or fork this repository! When contributing new MCP server configurations you can use the `/add-new-mcp` command to help with the process

```bash
/add-new-mcp {mcp-server-name}.json
```
