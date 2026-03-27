# add-new-mcp Custom Command

This command helps streamline the process of adding new MCP server configurations to the repository.

## Usage

```bash
/add-new-mcp {mcp-server-name}.json
```

Example:

```bash
/add-new-mcp github.json
```

## Instructions for Implementation

When adding a new MCP server configuration, follow these steps:

1. **Read Json If Exists** with the specified name
2. **Create the JSON configuration file** with the specified name if not exists
3. **Add alias** to `.mcp-aliases` file for easy command-line access
    - Add also to claude-all alias.
    - If the server should be used from Cursor, follow **Cursor** below.
4. **Prefer HTTP-based MCP servers** when available (use `http` type over `stdio`)
5. **Update README.md** by adding the new server to the MCP Servers table.
    - MCP Servers should be sorted alphabetically by name
6. **Add environment variables** to `.env.example` if the MCP server requires API keys or secrets
7. **Remind the user to reload their shell configuration** by running:
    ```bash
    source ~/.zshrc || source ~/.bashrc
    ```

## Cursor

Cursor reads MCP definitions from `.cursor/mcp.json` (`mcpServers`). The **JSON key** for each server is the identifier passed to `cursor mcp enable <identifier>` and `cursor mcp disable <identifier>` (case-sensitive).

When adding a new MCP that should work in Cursor:

1. Add an entry under `mcpServers` in `.cursor/mcp.json` with the chosen identifier as the key.
2. In `.mcp-aliases`, add:
   - `cursor-<name>='set -a && source ~/mcp/.env && set +a && cursor mcp enable <identifier> && cursor'`
   - `cursor-disable-<name>='cursor mcp disable <identifier>'`
3. Append `&& cursor mcp disable <identifier>` to the existing `cursor-disable-all` alias so “disable all” stays complete.
