# Claude Code

Loading all MCP servers simultaneously in Claude Code consumes unnecessary context window space. Using aliases from this repository allows you to load only the specific MCP server you need, improving efficiency.

## Auto-loading .env variables

Add aliases to your shell config (run from this directory):

```bash
# For zsh users
echo "source $(pwd)/.mcp-aliases" >> ~/.zshrc

# For bash users
echo "source $(pwd)/.mcp-aliases" >> ~/.bashrc
```

Then reload and use:
```
source ~/.zshrc
source ~/.bashrc
claude-ref  # Uses ref.json with auto .env loading
```

## MCP Servers

| Server | Category | Description |
|--------|----------|-------------|
| Playwright | Testing | Browser automation and web testing capabilities |
| Context7 | Documentation | Upstash's context management service for storing and retrieving contextual data |
| Ref | Documentation | HTTP-based MCP server for API reference and tools |
| Sequential Thinking | AI | MCP server that provides sequential thinking capabilities for enhanced reasoning |