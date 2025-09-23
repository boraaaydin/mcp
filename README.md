# Claude Code

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

| Server | Description |
|--------|-------------|
| Playwright | Browser automation and web testing capabilities |
| Context7 | Upstash's context management service for storing and retrieving contextual data |
| Ref | HTTP-based MCP server for API reference and tools |
| Sequential Thinking | MCP server that provides sequential thinking capabilities for enhanced reasoning |