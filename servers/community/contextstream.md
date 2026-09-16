# ContextStream MCP Server

Community MCP for shared project context across AI coding agents — code search plus decisions, lessons, and plans.

**Source:** [github.com/contextstream/mcp-server](https://github.com/contextstream/mcp-server)  
**Homepage:** [contextstream.io](https://contextstream.io)

## Installation

Hosted (Streamable HTTP):

```text
https://mcp.contextstream.io/mcp
```

Local launcher (Node.js 20+):

```bash
npx -y @contextstream/mcp-server@latest setup
```

Shell installer (macOS / Linux):

```bash
curl -fsSL https://contextstream.io/mcp/install.sh | sh
```

## Configuration

```json
{
  "mcpServers": {
    "contextstream": {
      "url": "https://mcp.contextstream.io/mcp"
    }
  }
}
```

Or with the npm launcher:

```json
{
  "mcpServers": {
    "contextstream": {
      "command": "npx",
      "args": ["-y", "@contextstream/mcp-server@latest"]
    }
  }
}
```

## Tools

| Tool | Description |
|------|-------------|
| `search` | Search the indexed codebase and cite sources |
| `context` | Load relevant project context, lessons, and rules for the current task |
| `capture_plan` | Save an implementation plan for later sessions |
| `session` | Capture decisions and lessons so later work stays aligned |

## Example

```
User: "Find the files for the next auth change and any saved decisions that should guide it."
Agent: [calls search] → [calls context / retrieves decisions] → cites sources and continues with shared project context
```
