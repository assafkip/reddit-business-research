# Reddit Business Research

**Find out what Reddit really thinks about your business, your competitors, and your market.**

This is a **plugin for [Claude Code](https://claude.ai/claude-code)** -- Anthropic's AI coding tool. It connects to Reddit's public data and runs a structured research workflow that finds relevant conversations, analyzes what people are saying, and delivers a report you can actually use.

No API keys. No setup headaches. Just install and go.

> **This is a Claude Code plugin, not a web app.** It doesn't have a UI, a server, or a preview screen. It works by adding new capabilities to Claude inside your conversations. You install it once, then use it by typing a command in chat.

---

## What you get

A markdown report with:

- **Executive summary** -- the 3-5 things you need to know right now
- **What people love** -- positive mentions, recommendations, praise (with links)
- **Pain points** -- what frustrates people in your space (with links)
- **Feature requests** -- what your audience wishes existed (with links)
- **Competitor landscape** -- how people compare you to alternatives (with links)
- **Where your audience lives** -- the subreddits that matter for your business
- **Threads worth engaging** -- high-visibility conversations where you could add value
- **Gaps and opportunities** -- questions nobody is answering well

Every finding links directly to the Reddit thread so you can read it yourself.

---

## How it works

1. You tell Claude about your business, competitors, and what you want to learn
2. Claude searches Reddit across relevant keywords and subreddits
3. It reads through the most relevant posts and comment threads
4. It categorizes everything and writes a structured report
5. The report saves as a local file on your machine

The whole thing takes a few minutes depending on how much is out there.

---

## Install

### What you need first

1. **Claude Code** -- [Install here](https://claude.ai/claude-code) if you don't have it
2. **uv** (Python package runner) -- [Install here](https://docs.astral.sh/uv/getting-started/installation/) if you don't have it:

   **Mac / Linux:**
   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

   **Windows (PowerShell):**
   ```powershell
   powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
   ```

### Install the plugin

In the Claude Code **terminal** (not the chat), run:

```bash
claude /plugin install github:4-points-consulting/reddit-business-research
```

That's it. The Reddit connection is bundled -- no API keys, no extra config.

> **Using the Claude Code Desktop app?** Open the Terminal tab at the bottom of the screen and run the install command there. Do NOT use the "Preview" button -- this plugin has nothing to preview.

---

## Run it

Open Claude Code in any project folder and type **in the chat**:

```
/reddit-business-research:reddit-research
```

Claude will ask you:

1. What's your business? (name, what you do, who it's for)
2. What are you trying to learn? (brand sentiment, competitor intel, pain points, etc.)
3. Any competitors to track?
4. Keywords your audience uses
5. Subreddits you already know about (optional)

Then it runs the research and saves a report to `output/reddit-research-YYYY-MM-DD.md` in your current directory.

---

## Example use cases

**"I just launched and want to know if anyone's talking about us"**
- Search for your brand name, product name, founder name
- See if you're showing up in relevant subreddits
- Find early feedback before it becomes a pattern

**"I want to understand what my competitors are doing wrong"**
- List 2-3 competitors
- Get a breakdown of complaints, praise, and comparisons
- Find the gaps they're not filling

**"I need to figure out where my audience hangs out on Reddit"**
- Describe your ideal customer and what they care about
- Get a ranked list of subreddits with activity levels
- See what topics get the most engagement

**"I want to find content ideas and customer language"**
- Search for your industry keywords
- See what questions keep getting asked
- Steal the exact words your audience uses (for copy, landing pages, ads)

---

## FAQ

**Do I need a Reddit account?**
No. This uses Reddit's public data -- no login required.

**Does this cost anything?**
The plugin is free. Claude Code requires a subscription or API access.

**Is my data sent anywhere?**
No. Reports save as local markdown files on your machine. Nothing is uploaded.

**How often should I run this?**
Quarterly is a good rhythm. Sentiment shifts over time -- what's true today might not be in 3 months.

**Can I research a competitor without having my own business?**
Yes. Just describe the space and list the companies you want to research.

---

## File structure

```
reddit-business-research/
  .claude-plugin/
    plugin.json           # Plugin config (Reddit MCP bundled here)
  skills/
    reddit-research/
      SKILL.md            # The research workflow
  README.md               # This file
```

---

## Built by

[4 Points Consulting](https://github.com/4-points-consulting) -- threat intelligence and open source research for people who need answers.
