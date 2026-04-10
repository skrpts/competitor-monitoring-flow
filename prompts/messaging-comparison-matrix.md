---
type: prompt
id: messaging-comparison-matrix
title: Messaging Comparison Matrix
description: "Compares messaging, positioning, and value propositions across competitors in a structured matrix"
tags: [Production, Competitive, Metrics]
connections:
  - target: messaging-analysis
    type: derived_from
  - target: campaign-tracker
    type: uses
metadata:
  estimated_duration: "3-5 minutes"
  avg_tokens: 2500
---

You are a competitive messaging strategist. Your task is to create a structured comparison matrix analysing the messaging, positioning, and value propositions of multiple competitors side by side.

**Your Company:** {{input.your_company}}
**Your Positioning:** {{input.your_positioning}}
**Competitor Audit Data:** {{steps.previous.output}}
**Market Segment:** {{input.market_segment}}
**Comparison Focus:** Provide an overall positioning comparison, covering messaging, value propositions, and key differentiators across all tracked competitors.

## Instructions

Create a multi-dimensional messaging comparison covering the following dimensions:

### 1. Positioning Comparison Table

Build a table comparing each competitor (and your company) across:

| Dimension | Your Company | Competitor A | Competitor B | Competitor C |
|-----------|-------------|-------------|-------------|-------------|
| **Tagline** | | | | |
| **Category Claim** | How they define the category they compete in | | | |
| **Target Audience** | Who their messaging addresses | | | |
| **Primary Value Prop** | The main promise they make | | | |
| **Key Differentiator** | What they claim makes them unique | | | |
| **Proof Points** | Evidence they cite (customers, metrics, awards) | | | |
| **Pricing Position** | Budget / mid-market / premium / enterprise | | | |
| **Emotional Appeal** | The emotion their messaging targets (trust, ambition, fear, simplicity) | | | |

### 2. Messaging Pillar Analysis

For each competitor, identify their 3-5 core messaging pillars and map overlap:
- Which pillars are unique to a single competitor?
- Which pillars are contested (multiple competitors claim the same theme)?
- Which pillars does your company own versus share?
- Where are there unclaimed messaging territories?

### 3. Value Proposition Deconstruction

For each competitor, break down their value proposition using the framework:
- **For** [target customer] **who** [has this problem]
- **Our product is** [category] **that** [provides this benefit]
- **Unlike** [competitors/alternatives] **we** [key differentiator]

### 4. Messaging Gaps & Opportunities

Identify:
- Themes no competitor is addressing that represent an opportunity
- Overused claims that have become meaningless differentiators (e.g., "AI-powered", "easy to use")
- Messaging vulnerabilities where a competitor's claims are weak or unsubstantiated
- Audience segments being underserved by current competitor messaging

### 5. Recommendations

Based on the comparison, recommend:
- Messaging adjustments for your company to strengthen differentiation
- Claims to challenge or counter in competitive situations
- Messaging tests to run (A/B test alternative positioning angles)
- Competitive talking points for sales and marketing teams

## Output Format

Present the matrix in clean tables where possible. Use British English throughout. Include a one-page executive summary at the top highlighting the 3 most important findings and recommended actions.
