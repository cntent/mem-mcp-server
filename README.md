# Mem.ai MCP Server

MCP server for integrating Mem.ai with Claude using the Mem.ai v2 API.

## Version

2.1.0

## Setup

1. Deploy to Railway (or any Node.js hosting platform)
2. Add `MEM_API_KEY` environment variable with your Mem.ai API key
3. Optionally set `CORS_ORIGIN` to restrict cross-origin access (defaults to `*`)
4. Use the MCP endpoint in Claude.ai connectors

## Endpoints

- **MCP (Streamable HTTP - Recommended)**: `https://your-app.railway.app/mcp`
- **SSE (Legacy)**: `https://your-app.railway.app/sse`
- **Health check**: `https://your-app.railway.app/health`
- **Info**: `https://your-app.railway.app/`

## Available Tools

### Notes Management
- `mem_search` - Search notes using semantic search (with filters for collections, tasks, images, files)
- `mem_list` - List notes with filtering and cursor-based pagination
- `mem_create` - Create new notes with optional collection assignment and custom timestamps
- `mem_read` - Read specific notes by ID

### Intelligent Processing
- `mem_it` - Send content to Mem.ai for intelligent processing and organization (async)

### Collections
- `mem_collections_list` - List all collections
- `mem_collections_search` - Search for collections

## API Reference

For detailed API documentation, visit: https://docs.mem.ai/api-reference/overview/introduction

## Requirements

- Node.js >= 18.0.0
- Mem.ai API key

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `MEM_API_KEY` | Yes | Your Mem.ai API key |
| `PORT` | No | Server port (default: 3000) |
| `CORS_ORIGIN` | No | Allowed CORS origin (default: `*`) |

## Dependencies

- `@modelcontextprotocol/sdk` - MCP protocol implementation
- `express` - Web server
- `zod` - Schema validation
