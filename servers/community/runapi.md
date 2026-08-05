# RunAPI MCP Server

Community MCP server for RunAPI - browse available models, check runtime pricing, create media tasks, poll task status, and check account balance.

**Source:** [github.com/runapi-ai/mcp](https://github.com/runapi-ai/mcp)

## Installation

```bash
npx -y @runapi.ai/mcp
```

## Configuration

```json
{
  "mcpServers": {
    "runapi": {
      "command": "npx",
      "args": ["-y", "@runapi.ai/mcp"],
      "env": {
        "RUNAPI_API_KEY": "<your-api-key>"
      }
    }
  }
}
```

## Tools

| Tool | Description |
|------|-------------|
| `list_models` | List RunAPI models from the embedded catalog |
| `get_model_info` | Inspect model inputs, constraints, and service/action details |
| `check_pricing` | Check current runtime pricing for a model action |
| `create_task` | Create an authenticated media generation task |
| `get_task` | Poll an existing task status and result |
| `check_balance` | Check account balance and spending metrics |

## Use Case

Let MCP-compatible coding agents discover RunAPI model options and run image, video, audio, music, and other model API jobs from a local tool session.
