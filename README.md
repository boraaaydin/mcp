# MCP Server Definitions for Claude Code

Loading all MCP server simultaneously in Claude Code consumes unnecessary context window space. Claude Code allows you to load a single MCP server before any session.
This repository stores some of the most commonly used MCP server so you can use them with ease.

## Mac & Linux - use with aliases

```zsh
# Copy environment variables template
cp .env.example .env

# For zsh users
echo "source $(pwd)/.mcp-aliases" >> ~/.zshrc
source ~/.zshrc

# For bash users
echo "source $(pwd)/.mcp-aliases" >> ~/.bashrc
source ~/.bashrc
```

## Windows

### Setting API Keys (if required by MCP server)

```cmd
# Option 1: Temporary (current session only)
set XYZ_API_KEY=your_api_key_here

# Option 2: Permanent (system-wide)
setx XYZ_API_KEY "your_api_key_here"
```

### Running Claude Code with MCP Servers

```cmd
# Close and reopen terminal after setting API keys, then run:
claude --mcp-config server\{mcp-server-name}.json

# Examples:
claude --mcp-config server\playwright.json
claude --mcp-config server\github.json
```


## MCP Servers

| Server | Alias | Category | Description |
|--------|-------|----------|-------------|
| Agent Zero | `claude-agent-zero` | AI Framework | Agent Zero AI framework with autonomous task execution capabilities |
| Apify | `claude-apify` | Web Scraping | Web scraping and automation platform with actor-based workflows |
| BrowserMCP | `claude-browsermcp` | Testing | Browser automation and web scraping capabilities |
| Chrome DevTools | `claude-chrome-devtools` | Testing | Chrome DevTools Protocol integration for browser debugging and automation |
| Context7 | `claude-context7` | Documentation | Upstash's context management service for storing and retrieving contextual data |
| GitHub | `claude-github` | Development | GitHub integration for repository management and code collaboration |
| Playwright | `claude-playwright` | Testing | Browser automation and web testing capabilities |
| Ref | `claude-ref` | Documentation | HTTP-based MCP server for API reference and tools |
| Sequential Thinking | `claude-sthink` | Thinking | MCP server that provides sequential thinking capabilities for enhanced reasoning |
| Supabase | `claude-supabase` | Database | PostgreSQL database and backend-as-a-service integration |
| Vercel | `claude-vercel` | Deployment | Deploy and manage serverless functions and web applications |

## Contributing

Feel free to contribute or fork this repository! When contributing new MCP server configurations you can use the `/add-new-mcp` command to help with the process

```bash
/add-new-mcp server/{mcp-server-name}.json
```
