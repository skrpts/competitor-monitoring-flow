---
type: skill
id: market-signal-detection
title: Market Signal Detection
description: "Identifies and interprets significant competitive signals from market activity, announcements, and behavioural changes"
tags: [Production, Tested, analysis:competitive, data:metrics]
connections:
  - target: llm-service
    type: runs_on
  - target: competitive-marketing-framework
    type: references
metadata:
  estimated_duration: "4-6 minutes"
  avg_tokens: 2500
---

## Capability

Monitors and interprets market signals from competitors and the broader competitive landscape. Detects meaningful changes in competitor behaviour, market dynamics, and industry trends that could represent threats or opportunities. Distinguishes between noise and genuine strategic signals.

## When to Use

- During regular competitive monitoring cycles
- When industry news or events might affect the competitive landscape
- After a competitor makes a public announcement (funding, product launch, partnership)
- When market conditions shift (regulatory changes, economic events, technology disruptions)
- Before strategic planning sessions to ensure decisions are informed by current competitive reality

## Process

1. **Signal Collection** — Gather observable competitive activity from multiple sources:
   - Company announcements (press releases, blog posts, social media)
   - Product changes (new features, pricing changes, packaging updates)
   - Hiring patterns (job postings indicate strategic direction)
   - Partnership and integration announcements
   - Funding rounds and financial disclosures
   - Conference appearances and speaking topics
   - Patent filings and research publications
   - Customer reviews and sentiment shifts

2. **Signal Classification** — Categorise each signal by type:
   - **Strategic:** Changes in company direction, market focus, or positioning
   - **Tactical:** Campaign launches, feature releases, pricing adjustments
   - **Operational:** Hiring patterns, office expansions, restructuring
   - **Market:** Industry trends, regulatory changes, technology shifts
   - **Customer:** Sentiment changes, review patterns, churn indicators

3. **Significance Assessment** — Evaluate each signal for:
   - **Impact potential:** How much could this affect your market position? (high/medium/low)
   - **Certainty:** How confident are we in the interpretation? (confirmed/likely/speculative)
   - **Urgency:** How quickly does this require a response? (immediate/near-term/monitor)
   - **Reversibility:** Is this a committed move or easily reversed?

4. **Pattern Recognition** — Look for signal clusters that indicate broader strategic shifts:
   - Multiple hiring posts in a new technology area = potential product pivot
   - Pricing reductions + aggressive advertising = market share grab
   - Partnership announcements + integration launches = ecosystem play
   - Executive departures + messaging changes = strategic reset

5. **Implication Mapping** — For each significant signal, map out the potential implications:
   - What does this mean for our market position?
   - Which of our customers or prospects might be affected?
   - What opportunities does this create for us?
   - What threats does this pose?
   - What additional information would we need to confirm the interpretation?

## Inputs

- Observed competitor activity since last monitoring cycle
- Industry news and announcements
- Market data or trend reports
- Customer feedback or sales intelligence
- Previous signal reports for trend comparison

## Outputs

- Signal report with classified and assessed signals
- Pattern analysis identifying strategic shifts
- Implication map for significant signals
- Recommended monitoring adjustments (new signals to track, signals to deprioritise)
- Escalation recommendations for high-impact signals

## Constraints

- Do not over-interpret isolated signals — a single job posting is not a strategic pivot
- Always assess confidence level and state assumptions clearly
- Distinguish between public information and speculation
- Avoid confirmation bias — look for disconfirming evidence alongside supporting evidence
- Be explicit about information gaps and what additional data would strengthen the analysis
