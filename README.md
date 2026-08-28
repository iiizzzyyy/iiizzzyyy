# Hi, I'm Izzy

I build orchestration layers that connect coding agents to the tools operators already use. Founder of [PromptMetrics](https://www.promptmetrics.dev) in Berlin. I come from the CRM side, so I build for the people who live in these systems every day.

My focus: agents that touch production CRM data need safety rails, not vibes. Every write gated behind preview and approval. Undo snapshots. Audit logs you can read like a spec.

## What I'm building

**[hubspot-claude](https://github.com/promptmetrics/hubspot-claude)** — Claude Code plugin for HubSpot CRM admin. 44 sub-agents and 79 tools today (counts drift — the CLI is the source of truth). Human-in-the-loop on every write. Includes a runtime learning loop that extracts workflow blueprints from existing portals and turns them into reusable templates.

**[hubspot-mcp](https://github.com/promptmetrics/hubspot-mcp)** — Standalone MCP server for HubSpot. 76 domain tools plus 5 safety tools (approve, reject, pending, audit, undo). Built for clients that can't run Claude Code plugins.

**[whoop-relay](https://github.com/promptmetrics/whoop-relay)** — Multi-user MCP server on Cloudflare Workers that connects WHOOP accounts to Claude (claude.ai, Desktop, Code, Cowork). Webhooks land in a queue, a consumer resolves the data within WHOOP's rate limits into D1, and the server answers "how did I sleep, should I push today?" instantly — no API quota burned per question. Ships an interactive dashboard rendered inside the chat (MCP Apps) plus an authenticated live dashboard on the web.

**[promptmetrics](https://github.com/iiizzzyyy/promptmetrics)** — Lightweight, self-hosted prompt registry. GitHub-backed versioning and metadata logging for LLM observability.

**[clawlens](https://github.com/iiizzzyyy/clawlens)** — Investigation layer for OpenClaw. Answers the question "why did my agent do that?"

## How I think about agent safety

Approval friction should match risk. Reads are free. Single writes get a preview and a yes. Bulk writes require a typed record count, re-checked at execution. Large operations run a 5-record sample before they scale. I wrote about this on [LinkedIn](https://www.linkedin.com/in/iizzyy/).

## Elsewhere

- Website: [promptmetrics.dev](https://www.promptmetrics.dev)
- X: [@iiizzy](https://x.com/iiizzy)
- Community: Operator Stack on Skool, for RevOps and CS people running 3+ tools

Tell me where I'm wrong. Issues and PRs welcome.
