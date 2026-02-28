# Agentic Ads Prompts

A prompt library for advertising product managers and operators working with LLMs. Built from real problems in ad tech - supply-side, demand-side, publisher monetization, and campaign management.

This is not a generic PM prompt library. Every prompt here was written for the specific reasoning challenges that come up in advertising product work: yield tradeoffs, targeting logic, partner integrations, performance diagnostics, and monetization strategy.

---

## Who This Is For

- PMs building ad products at publishers, DSPs, SSPs, or retail media networks
- Operators managing campaign performance across channels
- Anyone trying to use AI to move faster on advertising problems without reinventing the prompts every time

---

## Structure

| Folder | What's Inside |
|---|---|
| `campaign-analysis/` | Prompts for diagnosing performance, explaining variance, and summarizing results for stakeholders |
| `audience-targeting/` | Prompts for reasoning about segmentation, overlap, exclusions, and frequency strategy |
| `publisher-monetization/` | Prompts for yield optimization, floor pricing, fill rate analysis, and demand partner strategy |
| `prd-and-briefs/` | Prompts for drafting ad product specs, integration briefs, and technical requirements |
| `competitive-analysis/` | Prompts for breaking down competitor ad products and publisher monetization stacks |
| `agent-workflows/` | Multi-step agentic workflows for more complex, structured tasks |

---

## How to Use These

Each prompt is a standalone `.md` file. Copy the prompt, fill in the bracketed placeholders with your actual data or context, and paste into Claude, ChatGPT, or your LLM of choice.

The `agent-workflows/` folder contains more structured workflows designed for Claude with tools enabled - these are multi-step and expect the model to reason across several inputs before responding.

---

## Contributing

These prompts improve with use. If you work in ad tech and have a prompt that's saved you real time, open a PR. The goal is a library that reflects how this industry actually operates, not how it's described in textbooks.

---

*Built by [Freddy Porges](https://github.com/freddyporges-lgtm) as part of an exploration into AI-augmented advertising product work.*
