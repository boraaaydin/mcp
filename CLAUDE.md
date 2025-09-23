# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This is a **Claude Code MCP (Model Context Protocol) Configuration Repository**. It contains configuration files for extending Claude Code's capabilities through external MCP servers like:

- **Playwright MCP Server**: Browser automation and testing capabilities
- **Context7 MCP Server**: Upstash's context management service integration

## Architecture

This is a configuration-only repository with no source code. Each JSON file defines an MCP server configuration that can be loaded by Claude Code using the `--mcp-config` flag.

## Configuration Files

## Usage Commands

Start Claude Code with MCP server configurations:

```bash
# For Playwright capabilities
claude --mcp-config server/playwright.json

# For Context7 capabilities
claude --mcp-config server/context7.json

# Multiple configs can be combined
claude --mcp-config server/playwright.json --mcp-config server/context7.json
```

## Development Workflow

Since this is configuration-only:

1. **No build process** - configurations are used directly
2. **No testing framework** - MCP servers are tested through Claude Code usage
3. **No linting** - JSON files should be valid JSON format

## Dependencies

**Runtime Requirements:**

- Node.js (for `npx` commands)
- Bun (for `bunx` commands)
- Claude Code CLI

## Configuration Patterns

- Use `bunx -y` for Bun packages to auto-install latest versions
- Use `npx` for npm packages with `@latest` tag
- Environment variables for sensitive data (API keys)
- Modular approach: one MCP server per configuration file