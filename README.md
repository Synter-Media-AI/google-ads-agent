# Google Ads MCP Starter Kit — Manage Google Ads with AI

[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: Google Ads](https://img.shields.io/badge/Platform-Google%20Ads-4285F4)](https://ads.google.com)

**The fastest way to manage Google Ads with an AI agent.** Open this repo in Amp, Cursor, or VS Code and start managing Search campaigns, Performance Max, keywords, and bidding — all through natural conversation.

---

## Why Google Ads + AI?

Google Ads is the highest-intent advertising platform on the planet. When someone searches "best CRM for startups," they're actively looking to buy. But managing Google Ads well requires constant attention: adjusting bids, testing ad copy, adding negative keywords, monitoring Quality Scores, and interpreting GAQL reports.

AI agents eliminate the grunt work. Instead of clicking through the Google Ads UI, you describe what you want in plain English. The agent handles the API calls, validates your inputs, and executes changes — in seconds, not hours.

**Best for:** Intent-based marketing, lead generation, ecommerce, SaaS, local businesses — anyone who wants to capture demand when people are actively searching.

---

## Quick Start (30 Seconds)

### Amp / Cursor / VS Code (Copilot)

1. **Get a free API key** at [syntermedia.ai/developer](https://syntermedia.ai/developer)
2. **Set the key:**
   ```bash
   export SYNTER_API_KEY=syn_your_key_here
   ```
3. **Open this repo** in your editor
4. **Start chatting** — MCP tools are pre-configured in `.mcp.json`

### Claude Desktop

Copy `claude_desktop_config.json` to your Claude config directory and replace the API key:

- **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

---

## What You Can Do

| Capability | Example |
|-----------|---------|
| **Create Search Campaigns** | "Launch a Search campaign for 'project management software' with $50/day budget" |
| **Build Performance Max** | "Create a PMax campaign with my product feed targeting the US" |
| **Manage Keywords** | "Add 'free trial CRM' as a phrase match keyword to the SaaS campaign" |
| **Adjust Bids** | "Increase bids 20% on keywords with conversion rate above 5%" |
| **Write Ad Copy** | "Generate 15 responsive search ad headlines for our accounting software" |
| **Run GAQL Queries** | "Show me all campaigns spending over $100/day with ROAS below 2x" |
| **Monitor Quality Score** | "Which keywords have a Quality Score below 5? What's dragging them down?" |
| **Negative Keywords** | "Add 'free' and 'cheap' as campaign-level negative keywords" |
| **Smart Bidding** | "Switch the brand campaign from manual CPC to target ROAS of 400%" |
| **Geographic Targeting** | "Only show ads in California, Texas, and New York" |
| **Ad Schedule** | "Pause ads on weekends — we only convert Monday through Friday" |
| **Conversion Tracking** | "Set up a conversion action for newsletter signups" |

---

## Example Conversations

### 1. Launching Your First Search Campaign

> **You:** I want to run Google Ads for my SaaS product. It's a project management tool for remote teams. Budget is $75/day.
>
> **Agent:** I'll create a Search campaign targeting high-intent keywords. Here's my plan:
>
> - **Campaign:** "Project Management — Search"
> - **Budget:** $75/day
> - **Bidding:** Maximize Clicks (until we have 30+ conversions, then switch to Target CPA)
> - **Keywords:** "project management software," "remote team tools," "task management app," "team collaboration software" (phrase match)
> - **Negative keywords:** "free," "open source," "template"
> - **Geo:** United States
>
> Want me to proceed?
>
> **You:** Yes, but add Canada too.
>
> **Agent:** Done. Campaign created with 4 ad groups, 16 keywords, and 3 responsive search ads per group. Campaign is set to PAUSED — say "enable it" when you're ready to go live.

### 2. Diagnosing Poor Performance with GAQL

> **You:** My cost per lead jumped from $35 to $80 this week. What happened?
>
> **Agent:** Let me pull the data. Running GAQL query for the last 14 days segmented by day...
>
> Found the issue: Your top-performing keyword "enterprise project management" triggered a broad match expansion to "project management internship" starting Tuesday. That search term spent $340 with 0 conversions.
>
> **Recommended fix:**
> 1. Add "internship" as a negative keyword ✅
> 2. Switch that keyword from broad to phrase match
> 3. Review search terms report weekly
>
> Want me to apply these changes?

### 3. Scaling with Performance Max

> **You:** Search is working great — $40 CPA, 200 leads/month. What's next?
>
> **Agent:** With a proven $40 CPA on Search, you're ready for Performance Max. PMax will extend your reach to YouTube, Display, Discover, Gmail, and Maps — all from one campaign.
>
> I'll create a PMax campaign with:
> - Your existing headlines and descriptions from top Search ads
> - 5 landscape images + 5 square images (I can generate these)
> - Your proven audience signals as hints (not restrictions)
> - $50/day budget, Target CPA of $50 (starting 25% above Search to give PMax room to learn)
>
> The key with PMax: give it 2-3 weeks to optimize before judging performance. The algorithm needs ~50 conversions to stabilize.

### 4. Quality Score Deep Dive

> **You:** How's my Quality Score across the account?
>
> **Agent:** Here's the breakdown across 847 active keywords:
>
> | Quality Score | Keywords | % of Spend |
> |---|---|---|
> | 8-10 | 124 | 41% |
> | 6-7 | 298 | 35% |
> | 4-5 | 312 | 19% |
> | 1-3 | 113 | 5% |
>
> **Biggest opportunities:**
> - 113 keywords scoring 1-3 are costing you ~$2.40 more per click than necessary
> - Top offender: "cloud collaboration tools" (QS: 2) — landing page relevance is "Below Average"
> - Fix: Create a dedicated landing page for collaboration keywords. Expected savings: ~$1,800/month.

### 5. Budget Reallocation

> **You:** I have $3,000/month. How should I split it across my 5 campaigns?
>
> **Agent:** Based on last 30 days of performance:
>
> | Campaign | Current Budget | ROAS | Recommended |
> |---|---|---|---|
> | Brand | $600 | 12.4x | $500 (already capturing 95% of brand searches) |
> | Competitor | $700 | 1.8x | $400 (reduce — barely profitable) |
> | Product — Features | $600 | 4.2x | $900 (scale winner) |
> | Product — Pricing | $500 | 3.8x | $700 (scale second winner) |
> | Remarketing | $600 | 6.1x | $500 (limited audience pool) |
>
> This reallocation shifts $600 from underperformers to your two best campaigns. Expected impact: +15% overall ROAS.

---

## Google Ads Tips from the Pros

1. **Start with Search, graduate to PMax.** Search teaches you which keywords convert. Feed that data into PMax for broader reach.
2. **Minimum budget: $10/day per campaign.** Below this, Google's algorithm can't gather enough data to optimize. For competitive industries, $25-50/day is more realistic.
3. **GAQL is your superpower.** Most advertisers never touch the query language. Queries like `SELECT campaign.name, metrics.cost_micros WHERE metrics.conversions = 0 AND metrics.cost_micros > 500000000` instantly find money pits.
4. **Don't use broad match without Smart Bidding.** Broad match + manual CPC = wasted spend. Broad match + Target CPA = Google's algorithm finding conversions you'd miss.
5. **Check search terms weekly.** Even with exact match, Google's "close variants" can trigger surprising queries. Negative keywords are your defense.
6. **Conversion tracking before everything.** Never launch a campaign without verified conversion tracking. No tracking = no Smart Bidding = flying blind.
7. **Responsive Search Ads need variety.** Don't write 15 variations of the same headline. Give Google diverse options: feature-focused, benefit-focused, urgency-driven, social proof.

---

## FAQ

### Can Claude manage my Google Ads?
Yes. With this MCP starter kit, Claude (or any MCP-compatible agent) can create campaigns, adjust bids, add keywords, write ad copy, and pull performance reports — all through the Google Ads API.

### Do I need the Google Ads API?
No. The Synter MCP server handles API authentication and calls. You just need a free API key from [syntermedia.ai/developer](https://syntermedia.ai/developer).

### Is there an MCP for Google Ads?
This is it. This repo pre-configures the Synter MCP server for Google Ads management. Works with Amp, Cursor, VS Code, and Claude Desktop.

### Can the AI agent spend my money without asking?
Campaigns are created in PAUSED state by default. The agent will always confirm before enabling campaigns or making budget changes.

### What's GAQL?
Google Ads Query Language — a SQL-like language for querying your Google Ads data. It's far more powerful than the Google Ads UI for finding specific performance patterns. Example: `SELECT ad_group_criterion.keyword.text, metrics.ctr WHERE metrics.impressions > 1000 ORDER BY metrics.ctr ASC`.

### Can I use this with my existing Google Ads account?
Absolutely. Connect your Google Ads account via OAuth at [syntermedia.ai/settings](https://syntermedia.ai/settings/credentials), and the agent can manage your existing campaigns.

---

## Related Repos

- [meta-ads-agent](https://github.com/Synter-Media-AI/meta-ads-agent) — Facebook & Instagram Ads
- [microsoft-ads-agent](https://github.com/Synter-Media-AI/microsoft-ads-agent) — Bing Ads (30% lower CPCs)
- [google-analytics-agent](https://github.com/Synter-Media-AI/google-analytics-agent) — GA4 reports & conversion tracking
- [google-tag-manager-agent](https://github.com/Synter-Media-AI/google-tag-manager-agent) — Tag & pixel management
- [conversion-tracking-agent](https://github.com/Synter-Media-AI/conversion-tracking-agent) — Verify tracking setup
- [cross-platform-ads-agent](https://github.com/Synter-Media-AI/cross-platform-ads-agent) — Manage all platforms together

---

## License

MIT — see [LICENSE](LICENSE) for details.

Built by [Synter](https://syntermedia.ai) · [Get API Key](https://syntermedia.ai/developer) · [Documentation](https://syntermedia.ai/docs)
