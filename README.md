# Reddit Business Research

Find out what Reddit thinks about your business, competitors, and market. No API keys needed.

## Quick start

1. Open **Claude Code** (CLI, desktop app, or VS Code)
2. Paste this and hit enter:

```
/plugin install github:assafkip/reddit-business-research
```

3. Run the research:

```
/reddit-business-research:reddit-research
```

Claude asks 5 questions about your business, searches Reddit, and saves a report to `output/reddit-research-YYYY-MM-DD.md`.

## Prerequisites

- [Claude Code](https://claude.ai/claude-code)
- [uv](https://docs.astral.sh/uv/getting-started/installation/) (Python package runner)

```bash
# Install uv if you don't have it
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## What you get

A markdown report with linked Reddit threads covering:

- Executive summary
- What people love and hate
- Pain points and feature requests
- Competitor comparisons
- Relevant subreddits
- Threads worth engaging
- Market gaps

## Built by

[4 Points Consulting](https://github.com/4-points-consulting)
