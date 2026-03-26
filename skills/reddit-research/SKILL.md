---
name: reddit-research
description: Research what Reddit says about a business, its competitors, and its industry. Use when someone wants to understand Reddit sentiment, find competitor mentions, discover relevant subreddits, or identify market gaps. Generates a structured report with links.
argument-hint: "[business-name]"
allowed-tools: mcp__reddit__reddit_search, mcp__reddit__reddit_search_subreddit, mcp__reddit__reddit_get_subreddit_posts, mcp__reddit__reddit_get_post, mcp__reddit__reddit_get_user, mcp__reddit__reddit_get_user_posts, Write, Read, Glob
---

# Reddit Business Research

Research what Reddit says about a business, its competitors, and its industry.

## Step 1: Intake

Before doing anything, ask the user these questions and wait for their answers:

1. **What's your business?** Name, what you sell or do, and who it's for.
2. **What are you trying to learn?** Pick one or more:
   - Brand sentiment (what people say about you)
   - Competitor intel (how you compare to alternatives)
   - Pain points (what your target audience complains about)
   - Feature requests (what users wish existed)
   - Subreddit discovery (where your audience hangs out)
3. **Competitors?** List any competitor names to track alongside your brand.
4. **Keywords or jargon** your audience uses when talking about this space.
5. **Known subreddits** where your audience hangs out (optional -- we'll find more).

If the user provided a business name as an argument (`$ARGUMENTS`), use that as a starting point but still confirm the details above.

## Step 2: Discovery (Phase 1)

Using the Reddit MCP tools:

1. Use `reddit_search` to search for the business name, product name, and top 3 keywords. Run up to 5 searches (sort by relevance, then by top).
2. From results, identify the top 5-8 subreddits where relevant discussion happens.
3. For each top subreddit, use `reddit_get_subreddit_posts` to scan hot and top posts.
4. If competitors were provided, run `reddit_search` for each competitor name.

**Checkpoint:** After Phase 1, give the user a quick summary:
- Which subreddits look most active for their space
- How many relevant posts found
- Any surprises or unexpected communities

Ask if they want to adjust keywords or add subreddits before the deep dive.

## Step 3: Deep Dive (Phase 2)

1. Use `reddit_search_subreddit` to search the top 3-5 subreddits for specific queries (product name, competitor comparisons, pain point keywords).
2. For the 5-10 most relevant or high-engagement posts, use `reddit_get_post` to pull the full comment thread.
3. Read through comments for:
   - Sentiment (positive, negative, mixed)
   - Specific praise
   - Specific complaints
   - Feature requests
   - Competitor comparisons
   - Questions people keep asking

## Step 4: Synthesis (Phase 3)

Analyze everything collected and categorize into:

- **Positive mentions** -- what people like, recommend, praise
- **Pain points** -- complaints, frustrations, unmet needs
- **Feature requests** -- what users wish existed
- **Competitor talk** -- how competitors are discussed, who gets recommended and why
- **Recurring questions** -- what keeps getting asked without a good answer
- **Engagement opportunities** -- threads where the business could add value by responding

## Step 5: Report

Generate a markdown report and save to `output/reddit-research-YYYY-MM-DD.md` (create the output/ directory if it doesn't exist). The report must include:

### 1. Executive Summary
3-5 bullets -- the big takeaways.

### 2. What People Love
Positive mentions, praise, recommendations. Include direct Reddit links for each.

### 3. Pain Points and Complaints
Recurring issues, frustrations, unmet needs. Include direct Reddit links.

### 4. Feature Requests
What users say they want but can't find. Include direct Reddit links.

### 5. Competitor Landscape
How competitors are mentioned, head-to-head comparisons. Include direct Reddit links.

### 6. Where Your Audience Lives
Top subreddits ranked by relevance. For each:
- Subreddit name and subscriber count (if available)
- Activity level (hot posts per day)
- Relevance to the business
- Sample thread titles

### 7. Threads Worth Engaging
High-visibility threads where a response from the business could add value. For each:
- Direct link
- Why it matters
- Suggested angle (not a script -- just the approach)

### 8. Gaps and Opportunities
- Topics nobody is covering well
- Questions that keep getting asked without good answers
- Underserved communities in their space

**Every finding must include a direct Reddit link** so the user can read the threads themselves.

Tell the user where the report was saved and offer to dig deeper into any section.

## Rules

- All research uses public Reddit data only
- Include direct links to every post/thread referenced
- Be honest about what you didn't find -- gaps are useful intel too
- If a search returns nothing, say so -- don't pad the report
- Distinguish between widely-held views (many posts) vs. one-off complaints
