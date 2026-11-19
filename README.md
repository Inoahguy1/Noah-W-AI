# Noah W: AI portfolio

I build AI agents and automations, mostly with Claude and Claude Code. I run
[Truevine Automation](https://truevineautomation.com), my freelance business that builds AI
tools for small businesses.

I designed every project below and built it with Claude Code as my pair programmer. I set the
goals and the rules, and I review and test every change. Each project has a write-up with what
it does, how it works, and what it shows. The source code is private, and I'm happy to walk
through it or give a live demo. All sample data is made up.

## AI projects

| Project | What it does | Tech |
|---|---|---|
| [Lead Qualifier Agent](projects/lead-qualifier-agent.md) | A Claude agent that looks up a lead with tools, scores it against a rubric, returns checked JSON, and drafts a follow-up that a person approves. Includes evals. 116 tests. | Python, Claude API (tool use, structured output), Pydantic |
| [Leads MCP Server](projects/leads-mcp-server.md) | An MCP server that gives Claude safe access to a lead CRM, built to handle agent retries, guessed ids and skipped steps. 42 tests. | Python, MCP SDK |
| [Claude Code Team Workflow](projects/claude-code-team-workflow.md) | My setup for rolling out Claude Code to a team safely: permission rules, hooks that block destructive commands, protected secrets, an audit log, review agents and CI. 210 tests. | Claude Code, Python, GitHub Actions |
| [Truevine Workspace](projects/truevine-workspace.md) | A self-hosted chat where people and AI agents share rooms. Mention an agent and it answers, running on a linked computer's own Claude Code. 72 tests. | Python (no dependencies), SQLite, JavaScript |
| [Truevine Systems](projects/truevine-systems.md) | AI systems for small service businesses: voice note to finished report, intake and follow-up, and a company brain that answers from the business's own notes. 57 tests. | Python, SQLite, Obsidian, Whisper, Claude Code |
| [Truevine CRM](projects/truevine-crm.md) | The CRM for my business: pipeline, calendar, website bookings, n8n hooks for AI follow-up, and safe contact enrichment. | Supabase, Postgres, TypeScript, JavaScript |
| [Truevine website](projects/truevine-website.md) | My business website, built with Claude. Live at [truevineautomation.com](https://truevineautomation.com). | React, CSS, GitHub Pages |

Test counts are from running each project's test suite. The tests run offline, with no API key.

## What I work with

Claude API · Claude Code (hooks, skills, subagents, MCP) · MCP servers · AI agents and evals ·
Python · JavaScript · TypeScript · Supabase / Postgres · n8n · GitHub Actions

## Contact

[LinkedIn](https://linkedin.com/in/noah-williams11) · [truevineautomation.com](https://truevineautomation.com)
