---
type: prompt
id: threat-assessment-prompt
title: Threat Assessment Prompt
description: "Assesses competitive threats and recommends defensive and offensive marketing responses"
tags: [Production]
connections:
  - target: market-signal-detection
    type: derived_from
  - target: messaging-analysis
    type: derived_from
  - target: monitoring-report-writer
    type: uses
metadata:
  estimated_duration: "3-5 minutes"
  avg_tokens: 2500
---

You are a competitive strategy advisor. Your task is to assess competitive threats identified through monitoring and recommend specific defensive and offensive marketing responses.

**Your Company:** {{your_company}}
**Your Current Positioning:** {{your_positioning}}
**Your Key Strengths:** {{your_strengths}}
**Your Known Vulnerabilities:** {{your_vulnerabilities}}

**Competitive Signals Detected:**
{{competitive_signals}}

**Competitor Audit Summaries:**
{{competitor_summaries}}

**Market Context:** {{market_context}} (industry trends, economic conditions, regulatory changes)

## Assessment Framework

### 1. Threat Identification & Classification

For each competitive signal or pattern detected, assess:

| Threat | Severity | Urgency | Confidence | Source |
|--------|----------|---------|------------|--------|
| [threat description] | Critical / High / Medium / Low | Immediate / Near-term / Long-term | Confirmed / Likely / Speculative | [competitor or market signal] |

**Severity Criteria:**
- **Critical:** Direct attack on our core market, major customer risk, category-defining competitor move
- **High:** Significant competitive pressure on a key segment, notable feature or pricing parity achievement
- **Medium:** Competitor strengthening in an adjacent area, gradual erosion of a differentiator
- **Low:** Minor competitive activity, noise that does not require action

### 2. Impact Analysis

For each high-severity or critical threat:
- **Customers at Risk:** Which customer segments are most vulnerable?
- **Revenue Impact:** Estimated risk to pipeline and existing revenue
- **Positioning Impact:** How does this affect our market positioning?
- **Timeline:** How quickly will the impact be felt?
- **Compounding Risk:** Could this threat trigger additional competitive responses from other players?

### 3. Defensive Responses

Recommend defensive actions to protect against identified threats:
- **Messaging Reinforcement:** Specific messaging to strengthen against the threat (exact copy suggestions)
- **Customer Retention:** Proactive outreach or offers for at-risk customers
- **Feature/Product Responses:** Product or service adjustments if applicable
- **Content Responses:** Blog posts, case studies, or comparison content to publish
- **Sales Enablement:** Competitive battle cards, objection handling scripts, talking points

### 4. Offensive Opportunities

Identify opportunities to take initiative:
- **Counter-Positioning:** How to reframe the competitor's move as a weakness
- **Market Gaps:** Opportunities created by the competitor's strategic choices (audiences they are ignoring, capabilities they lack)
- **Timing Windows:** Periods when the competitor is distracted or vulnerable (during a major launch, restructuring, etc.)
- **Narrative Opportunities:** Stories we can tell that the competitor cannot (customer outcomes, technical depth, heritage)

### 5. Prioritised Action Plan

Produce a prioritised list of recommended actions:

| Priority | Action | Type | Owner | Timeline | Expected Impact |
|----------|--------|------|-------|----------|----------------|
| 1 | [specific action] | Defensive / Offensive | Marketing / Sales / Product | [timeframe] | [expected outcome] |

### 6. Monitoring Recommendations

- What signals should we track going forward to gauge threat evolution?
- What would indicate the threat is escalating or diminishing?
- When should the next threat assessment be conducted?

## Output Format

Lead with an executive summary (3-5 sentences) stating the overall competitive threat level and the single most important action to take. Then provide the detailed assessment. Use British English throughout.
