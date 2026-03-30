# Reddit Business Research Plugin

This folder is a Claude Code plugin. It is not a web app or a runnable server.

## How to use this

1. Install it as a plugin: `claude /plugin install github:4-points-consulting/reddit-business-research`
2. Then type `/reddit-business-research:reddit-research` in any Claude Code conversation to start a research session.

## If the Reddit tools aren't available

Make sure `uv` is installed on your system. The plugin uses `uvx reddit-no-auth-mcp-server` to connect to Reddit's public data. No API keys needed.

- Mac/Linux: `curl -LsSf https://astral.sh/uv/install.sh | sh`
- Windows: `powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`
