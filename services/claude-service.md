---
type: service
id: claude-service
title: Claude Service
description: "How this skrpt uses Anthropic Claude for competitive intelligence gathering, analysis, and strategic recommendation"
tags: [Production, Tested]
connections: []
metadata:
  provider: "anthropic"
  model: "claude-sonnet"
  estimated_duration: "N/A"
---

## Claude Service — Competitor Monitoring Flow

This skrpt uses Anthropic Claude as its primary AI service for competitive intelligence analysis, messaging deconstruction, and strategic threat assessment.

### Usage Pattern

Claude is invoked at each stage of the monitoring pipeline:

1. **Competitor Auditing** — Claude analyses competitor websites, social media profiles, and marketing materials to produce structured audit reports. This requires the ability to systematically evaluate marketing presence across channels and extract meaningful insights from public information.

2. **Messaging Analysis** — Claude deconstructs competitor messaging to identify value propositions, positioning strategies, and messaging pillars. This requires nuanced understanding of marketing language, persuasion tactics, and brand communication patterns.

3. **Market Signal Detection** — Claude evaluates competitive signals and market developments to identify significant changes in the competitive landscape. This requires pattern recognition, the ability to distinguish noise from signal, and contextual understanding of market dynamics.

4. **Campaign Tracking** — Claude analyses competitor marketing campaigns to extract tactics, messaging strategy, and strategic intent. This requires understanding of multi-channel marketing, campaign mechanics, and competitive strategy.

5. **Threat Assessment** — Claude evaluates competitive threats and recommends defensive and offensive responses. This requires strategic thinking, risk assessment, and the ability to translate analysis into actionable recommendations.

6. **Report Compilation** — Claude synthesises all monitoring outputs into a cohesive periodic report. This requires information synthesis, prioritisation, and executive-level communication.

### Configuration

- **Temperature:** 0.3 for factual analysis (auditing, signal detection), 0.5 for strategic assessment (threat analysis, response recommendations)
- **Max tokens:** 3500 per invocation, 4000 for report compilation
- **Context window:** Monitoring is cumulative. Each stage builds on previous outputs. Previous period reports provide baseline context.

### Web Search Integration

This skrpt benefits significantly from web search capabilities. Claude can use web search to:
- Access current competitor website content and social media activity
- Identify recent press releases, announcements, and news coverage
- Verify claims and data points from competitor marketing materials
- Discover competitor job postings, patent filings, and partnership announcements

When web search is unavailable, the user must provide competitor content and market signals as input. The analysis quality depends directly on the completeness of the input provided.

### Requirements

- An active Anthropic API key or Claude CLI access
- Sufficient token quota for the full monitoring cycle (approximately 18,000-25,000 tokens per complete run)
- Optional: web search access for real-time competitive data
