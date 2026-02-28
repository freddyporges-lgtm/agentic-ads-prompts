# Agent Workflows

These are multi-step workflows designed for Claude with tools enabled. Unlike the single prompts in other folders, these are structured sequences where the agent reasons across multiple inputs before producing output. Best used with Claude in an agentic setup (Claude Code, API with tools, or Claude.ai with relevant connectors).

---

## 1. Campaign Health Monitor

A structured workflow for a weekly or daily campaign health check across a portfolio. The agent reviews performance data, flags issues, and produces a prioritized action list.

```
You are an ads performance analyst. I'm going to give you performance data for a portfolio of active campaigns. Your job is to:

Step 1 - Triage: Review all campaigns and classify each as (a) healthy, (b) needs monitoring, or (c) needs immediate action. Explain your classification for each.

Step 2 - Diagnose: For any campaign classified as (b) or (c), identify the most likely root cause of the issue. Use the data provided and flag where more information is needed.

Step 3 - Prioritize: Rank the campaigns needing action by revenue or performance impact. Tell me which to address first and why.

Step 4 - Recommend: For each campaign needing action, provide a specific recommended change (bid adjustment, targeting tweak, budget reallocation, creative swap, etc.) with the reasoning behind it.

Step 5 - Summarize: Produce a concise briefing I can share with the team or a stakeholder. Lead with the most important thing, then the supporting detail.

Here is the campaign data:
[paste your campaign performance data - can be a CSV, table, or bullet list]

Additional context:
- Campaign goals: [description]
- Any recent changes: [description]
- Budget constraints: [any limits on changes I can make]
```

---

## 2. Publisher Yield Audit Workflow

A structured workflow for auditing a publisher's full programmatic setup and producing a prioritized optimization plan.

```
You are a yield optimization specialist. I'm going to walk you through my programmatic setup. Your job is to conduct a structured audit and produce an optimization plan.

Work through this in order:

Step 1 - Inventory assessment: Review my inventory profile and identify the segments with the most optimization potential.

Step 2 - Demand stack review: Evaluate my demand partner setup and flag redundancies, gaps, or likely cannibalization.

Step 3 - Pricing analysis: Assess my floor price strategy and identify where I'm likely leaving money on the table.

Step 4 - Technical setup review: Flag any technical configuration issues that could be suppressing fill rate or CPM.

Step 5 - Prioritized recommendations: Rank your recommendations by expected revenue impact. For each, tell me what to change, how to test it, and how long before I'll see results.

My setup:

Inventory:
- Formats: [list]
- Traffic: [volume, device split, geo mix]
- Ad slots: [description of placements]

Demand:
- SSPs: [list]
- Deal types active: [open auction / PMP / preferred / PG]
- Header bidding: [setup description]
- Waterfall (if applicable): [priority order]

Current performance:
- Fill rate: [X%]
- Average CPM: [$X]
- RPM: [$X]
- Revenue trend: [last 90 days]

Known issues:
[Anything you already suspect]
```

---

## 3. New Ad Product Opportunity Assessment

A workflow for evaluating whether a new ad product or format is worth building. Takes market signals, internal data, and strategic context and produces a build/don't build recommendation.

```
You are a product strategist specializing in advertising. I'm evaluating whether to build a new ad product. Work through this assessment in steps and give me a clear recommendation at the end.

Step 1 - Problem validation: Is the problem real and large enough to justify building? Evaluate based on the context I provide.

Step 2 - Market landscape: Who else is solving this? What does the competitive environment look like?

Step 3 - Fit assessment: Is this a good fit for our business given our existing capabilities, customers, and strategic position?

Step 4 - Build vs. buy vs. partner: Is building the right approach, or should we consider acquiring or partnering?

Step 5 - Risk assessment: What are the biggest risks - technical, market, execution - and how serious are they?

Step 6 - Recommendation: Build, don't build, or explore further? Be direct and explain your reasoning.

Context:

The opportunity:
[Describe the ad product or feature you're considering]

The problem it solves:
[Who has this problem and how painful is it?]

Our current position:
- What we already have that's relevant: [capabilities, technology, customer relationships]
- What we'd need to build or acquire: [gaps]
- Strategic priority this connects to: [description]

Market signals:
[Any evidence of demand - customer requests, competitor moves, industry trends]

Constraints:
- Engineering capacity: [available / limited / none]
- Timeline: [any pressure to move fast?]
- Budget: [rough sense of what's available]
```

---

## 4. Inbox Intelligence Digest (Personal Workflow)

A workflow for processing a batch of newsletters and content emails and surfacing what's actually worth reading. Designed for use with a Gmail MCP connection.

```
You are my information assistant. I subscribe to a lot of newsletters and industry content across ads, tech, product, parenting, finance, and travel. I want you to process the emails I give you and tell me what's actually worth my attention.

Work through this in steps:

Step 1 - Categorize: Sort the emails into categories (ads/industry, tech/product, personal, finance, travel, parenting, other).

Step 2 - Summarize: For each email, write one sentence on what it contains. No editorializing yet - just what it is.

Step 3 - Signal detection: Flag any email that contains: (a) something actionable I need to respond to or decide on, (b) a genuinely new or important idea I haven't seen covered elsewhere recently, or (c) time-sensitive information.

Step 4 - Recommend: Tell me which 3-5 emails are actually worth opening and why. Be selective. If nothing clears the bar, say so.

Step 5 - Discard: Tell me what I can safely delete or archive without reading.

Here are the emails:
[paste email subjects, senders, and snippets - or connect via Gmail MCP to retrieve directly]

My context:
- I work in ads product at PayPal
- I care most about: programmatic trends, AI in advertising, publisher monetization, and anything relevant to building ad products
- Things I can deprioritize: generic marketing advice, event invitations, anything I've seen covered multiple times already
```
