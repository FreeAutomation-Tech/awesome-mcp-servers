# Agent QA MCP Server

MCP interface for Agent QA — author, validate, run, inspect, and triage natural-language web and mobile tests.

**Source:** [github.com/vostride/agent-qa](https://github.com/vostride/agent-qa)

## Installation

Agent QA requires Node.js 24 or newer. Install it in the project under test, initialize the workspace, and install the required browser runtime:

```bash
npm install -D agent-qa
npx agent-qa init
npx agent-qa install-browsers --chromium
```

## Configuration

Run the MCP server from the initialized Agent QA workspace:

```json
{
  "mcpServers": {
    "agent-qa": {
      "command": "npx",
      "args": ["agent-qa", "mcp"],
      "cwd": "/absolute/path/to/your/project"
    }
  }
}
```

## Tools

Agent QA exposes 33 `agent_qa_*` tools. Representative tools include:

| Tool | Description |
|------|-------------|
| `agent_qa_discover` | Inspect available Agent QA capabilities and workflows |
| `agent_qa_create_test` | Create a natural-language test definition |
| `agent_qa_validate_test` | Validate a test before execution |
| `agent_qa_enqueue_test_run` | Start an individual test run |
| `agent_qa_enqueue_suite_run` | Start a complete test suite run |
| `agent_qa_get_run` | Inspect a run and its current status |
| `agent_qa_get_run_artifact` | Retrieve screenshots, traces, and other run artifacts |
| `agent_qa_classify_failure` | Classify a failed run for triage and repair |

The remaining tools cover test suites, hooks, logs, run steps, IDs, configuration, cancellation, and definition management.

## Example

```
User: "Create and run a test that signs in, adds an item to the cart, and verifies checkout."
Agent: [calls agent_qa_create_test, agent_qa_validate_test, and agent_qa_enqueue_test_run]
```

Agent QA keeps persistent test memory and can repair tests when application behavior changes. It also provides a dashboard, CLI, and three agent skills alongside the MCP interface.

## License

Agent QA is source-available under FSL-1.1-ALv2 and converts to Apache-2.0 two years after each release.
