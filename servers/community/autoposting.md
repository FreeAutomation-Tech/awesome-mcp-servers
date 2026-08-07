# Autoposting MCP Server

Remote MCP server for Autoposting — schedule, generate and publish social posts to X, LinkedIn, Instagram, Threads and YouTube from any MCP client.

**Source:** [github.com/Autoposting-ai/autoposting-mcp](https://github.com/Autoposting-ai/autoposting-mcp)

## Installation

Hosted — nothing to install. Streamable HTTP with OAuth 2.1 Dynamic Client Registration, so there is no client ID or secret to configure.

```bash
claude mcp add --transport http autoposting https://app.autoposting.ai/mcp
```

## Configuration

```json
{
  "mcpServers": {
    "autoposting": {
      "type": "http",
      "url": "https://app.autoposting.ai/mcp"
    }
  }
}
```

## Tools

69 tools in total. Tools are filtered per connection by OAuth scope, and every tool carries MCP annotations so a client can tell reads from writes.

| Tool | Description |
|------|-------------|
| `create-post` | Draft a post for one or more platforms |
| `rewrite-post` | Rewrite an existing post |
| `schedule-post` | Schedule a post for a future time |
| `publish-post` | Publish a post now |
| `list-posts` | List posts and their delivery state |
| `generate-ideas` | Generate content ideas with AI agents |
| `generate-carousel` | Build a carousel from a brief |
| `render-clip` | Clip and render video |
| `search-kb` | Search a knowledge base |
| `create-webhook` | Register a webhook for delivery events |

Grouped as: Posts 11 · Ideas and agents 13 · Brands 7 · Knowledge base 12 · Carousels 6 · Video clips 5 · Webhooks 6 · Organizations and account 9.

## Example

```
User: "Draft a LinkedIn post about our new release and schedule it for Tuesday 9am."
Agent: [calls create-post, then schedule-post]
```

## Docs

- [MCP overview](https://docs.autoposting.ai/mcp/overview)
- Server card: `https://app.autoposting.ai/.well-known/mcp/server-card.json`
