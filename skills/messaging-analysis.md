---
type: skill
id: messaging-analysis
title: Messaging Analysis
description: "Deconstructs competitor messaging to identify positioning strategies, value propositions, and messaging patterns"
tags: [Production, Tested, Competitive, Metrics]
connections:
  - target: llm-service
    type: runs_on
  - target: competitive-marketing-framework
    type: references
metadata:
  estimated_duration: "5-8 minutes"
  avg_tokens: 3000
---

## Capability

Analyses competitor marketing messaging across all channels to identify their core positioning strategy, value propositions, messaging pillars, and communication patterns. Produces a structured breakdown that reveals what a competitor is saying, who they are saying it to, and how they differentiate themselves in the market.

## When to Use

- During initial competitor auditing to establish a messaging baseline
- When a competitor rebrands, launches a new product, or shifts positioning
- Before developing or refreshing your own messaging strategy
- When entering a new market and assessing the messaging landscape
- During competitive pitches to understand how rivals are framing themselves

## Process

1. **Message Extraction** — Collect and catalogue messaging from the competitor's website (homepage, about page, product pages, pricing page), social media profiles (bios, post themes, ad copy), email communications (if available), press releases, and blog content. Identify the phrases, claims, and language patterns used repeatedly.

2. **Value Proposition Identification** — Distil the competitor's core value proposition: what they promise, to whom, and why the customer should choose them over alternatives. Look for explicit statements ("We help X do Y") and implicit positioning (pricing strategy, feature emphasis, customer testimonials they showcase).

3. **Messaging Pillar Mapping** — Identify the 3-5 key messaging pillars the competitor returns to consistently. These are the themes that underpin their marketing — for example, "enterprise security", "ease of use", "AI-powered automation", "best-in-class support". Map which channels emphasise which pillars.

4. **Audience Targeting Analysis** — Determine who the competitor's messaging is aimed at. Analyse:
   - Language complexity and jargon (technical vs. accessible)
   - Pain points addressed (what problems they claim to solve)
   - Aspirational messaging (what outcomes they promise)
   - Social proof selection (what types of customers they showcase)
   - Pricing language (value vs. premium vs. budget framing)

5. **Tone and Brand Voice Assessment** — Characterise the competitor's communication style: formal vs. casual, authoritative vs. approachable, data-driven vs. emotional, urgent vs. considered. Note any inconsistencies across channels.

6. **Differentiation Claim Analysis** — Identify how the competitor explicitly differentiates from alternatives. What claims do they make about being unique, better, or different? Evaluate whether these claims are substantiated or aspirational.

## Inputs

- Competitor website URL
- Competitor social media profiles (links or content samples)
- Competitor ad copy (if available)
- Competitor email communications (if available)
- Industry context and market segment

## Outputs

- Core value proposition statement (one sentence)
- Messaging pillars (3-5 themes with evidence)
- Target audience profile (inferred from messaging)
- Brand voice characterisation
- Differentiation claims with substantiation assessment
- Channel-specific messaging emphasis map
- Messaging strengths and vulnerabilities

## Constraints

- Base analysis on observable public messaging only — do not speculate about internal strategy without evidence
- Distinguish between what a competitor claims and what they can substantiate
- Note when messaging is inconsistent across channels, as this often signals a recent pivot or internal misalignment
- Avoid projecting intent — describe what the messaging does, not what the competitor might be thinking
