---
type: document
id: competitor-monitoring-playbook
title: Competitor Monitoring Playbook
description: "Step-by-step guide to establishing and running an ongoing competitor monitoring programme"
tags: [Production, Tested]
connections:
  - target: competitive-marketing-framework
    type: references
metadata:
  document_type: "playbook"
  audience: "marketing-teams"
---

## Competitor Monitoring Playbook

This playbook provides a practical guide to establishing and maintaining an ongoing competitor monitoring programme. It covers setup, execution, reporting, and continuous improvement.

### Getting Started

#### Step 1: Define Your Competitive Set

Not every company in your space warrants monitoring. Categorise potential competitors into tiers:

**Tier 1 — Direct Competitors (Monitor Closely)**
Companies that sell similar products to similar customers at similar price points. These are the competitors your sales team encounters in deals. Typically 3-5 companies.

**Tier 2 — Adjacent Competitors (Monitor Regularly)**
Companies that overlap partially — either in product capability, target market, or use case. They may not be in every deal, but they influence customer expectations. Typically 3-8 companies.

**Tier 3 — Emerging Threats (Watch List)**
Startups, new entrants, or companies from adjacent markets that could become direct competitors. Check quarterly rather than weekly. Typically 5-10 companies.

Avoid monitoring too many competitors. Five well-tracked competitors yield better intelligence than fifteen poorly tracked ones.

#### Step 2: Set Up Information Sources

For each Tier 1 and Tier 2 competitor, establish monitoring across:

**Automated Monitoring:**
- Google Alerts for competitor brand names, executive names, and product names
- Social media follow/subscribe on all active platforms
- Newsletter subscriptions (use a dedicated monitoring email address)
- Review site alerts (G2, Capterra, Trustpilot — whichever are relevant)
- Job board alerts for competitor hiring patterns

**Manual Monitoring (periodic):**
- Website audits (monthly for Tier 1, quarterly for Tier 2)
- Ad library checks (Meta Ad Library, Google Ads Transparency Centre)
- Conference and event attendance
- Customer interviews and win/loss analysis for competitive deals

#### Step 3: Establish Your Baseline

Before you can detect changes, you need a baseline. Run the competitor-audit-prompt for each Tier 1 competitor to create detailed initial profiles. Store these as your reference point for future comparison.

### Running the Monitoring Programme

#### Weekly Activities (30-45 minutes)

1. **Review alerts and signals** — Check Google Alerts, social media activity, and any competitor content published during the week
2. **Log notable signals** — Record anything significant using the market-signal-detection skill framework
3. **Quick assessment** — Does anything require immediate attention? If yes, run the threat-assessment-prompt

#### Fortnightly/Monthly Activities (2-3 hours)

1. **Messaging check** — Review Tier 1 competitor websites for messaging changes
2. **Campaign tracking** — Analyse any new campaigns using the campaign-tracker prompt
3. **Comparison update** — Update the messaging-comparison-matrix if significant changes occurred
4. **Report compilation** — Run the monitoring-report-writer prompt to produce the periodic report
5. **Distribution** — Share the report with marketing leadership, sales, and product teams

#### Quarterly Activities (half day)

1. **Full competitor audit** — Re-run full audits for all Tier 1 competitors
2. **Tier review** — Reassess competitor tier assignments. Should anyone move up or down?
3. **Trend analysis** — Review the past quarter's reports for emerging patterns
4. **Strategy session** — Present findings to leadership and align on competitive response priorities
5. **Programme review** — Is the monitoring cadence appropriate? Are we tracking the right competitors?

### Making Intelligence Actionable

The biggest failure in competitive monitoring is producing reports nobody acts on. Ensure every report includes:

1. **Clear recommendations** with named owners and deadlines
2. **Sales enablement updates** — battle cards, talk tracks, objection handlers
3. **Content opportunities** — comparison pages, thought leadership that counters competitor narratives
4. **Product feedback** — feature requests or roadmap considerations driven by competitive pressure

### Common Pitfalls

1. **Monitoring everything, acting on nothing** — Limit monitoring scope and focus on actionable intelligence
2. **Reactive-only posture** — Use monitoring to find offensive opportunities, not just respond to threats
3. **Confirmation bias** — Do not selectively track signals that confirm existing beliefs about competitors
4. **Stale intelligence** — Outdated competitive data is worse than no data. Maintain freshness discipline.
5. **Copying competitors** — The goal is informed differentiation, not imitation. Use intelligence to zig when they zag.
