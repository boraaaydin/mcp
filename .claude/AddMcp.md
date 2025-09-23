# AddMcp Custom Command

This command helps streamline the process of adding new MCP server configurations to the repository.

## Usage

```
/AddMcp {mcp-server-name}.json
```

Example:
```
/AddMcp github.json
```

## Instructions for Implementation

When adding a new MCP server configuration, follow these steps:

1. **Create the JSON configuration file** with the specified name
2. **Add alias** to `.mcp-aliases` file for easy command-line access
3. **Prefer HTTP-based MCP servers** when available (use `http` type over `stdio`)
4. **Update README.md** by adding the new server to the MCP Servers table
5. **Add environment variables** to `.env.example` if the MCP server requires API keys or secrets
