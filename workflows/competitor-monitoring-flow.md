---
type: workflow
id: competitor-monitoring-flow
title: Competitor Monitoring Flow
description: "Ongoing competitor marketing surveillance, messaging analysis, and response planning"
tags: [Production, Tested]
connections:
  - target: messaging-analysis
    type: uses
  - target: market-signal-detection
    type: uses
  - target: competitor-audit-prompt
    type: uses
  - target: messaging-comparison-matrix
    type: uses
  - target: campaign-tracker
    type: uses
  - target: threat-assessment-prompt
    type: uses
  - target: monitoring-report-writer
    type: uses
  - target: audience-segmentation
    type: uses
  - target: llm-service
    type: runs_on
  - target: competitive-marketing-framework
    type: references
  - target: competitor-monitoring-playbook
    type: references
  - target: brand-voice-guide
    type: references
metadata:
  estimated_duration: "30-45 minutes"
  trigger: manual
---

## Overview

This workflow establishes and executes an ongoing competitor monitoring programme. It moves from initial competitor auditing through messaging analysis, campaign tracking, threat assessment, and periodic reporting. Designed to run on a regular cadence (weekly, fortnightly, or monthly) to keep competitive intelligence current.

## Pipeline Stages

### Stage 1: Competitor Audit

**Input:** Competitor name, website URL, known social media profiles, any previous audit data

Invoke the **competitor-audit-prompt** to produce a thorough baseline audit of each competitor's marketing presence. This covers their website messaging, content strategy, social media activity, advertising presence, and market positioning.

**Output:** Structured competitor profile covering all marketing channels, messaging themes, and current positioning.

**Gate:** At least 2 competitors must be audited before proceeding to comparison stages. For initial setup, audit all tracked competitors. For ongoing monitoring, audit only competitors with significant changes detected.

### Stage 2: Messaging & Positioning Analysis

**Input:** Competitor audit outputs from Stage 1, your own company's messaging and positioning

Invoke the **messaging-analysis** skill to identify each competitor's core messaging pillars, value propositions, and positioning strategy. Then run the **messaging-comparison-matrix** prompt to produce a side-by-side comparison across all tracked competitors.

**Output:** Messaging comparison matrix showing how each competitor positions themselves, their key differentiators, and messaging gaps or overlaps.

### Stage 3: Campaign & Signal Tracking

**Input:** Competitor marketing activity observed since last monitoring cycle, industry news, market developments

Invoke the **market-signal-detection** skill to identify significant changes in the competitive landscape. Then run the **campaign-tracker** prompt to analyse specific campaigns or marketing initiatives observed from competitors.

**Output:** Campaign analysis reports and market signal alerts for notable competitive moves.

**Note:** This stage benefits significantly from web search access. Without it, the user must provide observed competitor activity as input.

### Stage 4: Threat Assessment

**Input:** All outputs from Stages 1-3, your company's current market position and strategic priorities

Invoke the **threat-assessment-prompt** to evaluate competitive threats and recommend defensive or offensive responses. This prioritises threats by severity and urgency.

**Output:** Threat assessment with prioritised response recommendations.

**Gate:** Only escalate to executive stakeholders if a high-severity threat is identified. Medium and low threats feed into the standard monitoring report.

### Stage 5: Report Compilation

**Input:** All outputs from Stages 1-4, previous monitoring reports for trend comparison

Invoke the **monitoring-report-writer** prompt to compile all findings into a structured periodic report using the **monitoring-report-template** format.

**Output:** Complete competitive monitoring report ready for distribution to stakeholders.

## Error Handling

- If a competitor's website or social profiles are inaccessible, document the gap and proceed with available information. Flag the data gap in the report.
- If no significant competitive changes are detected in a monitoring cycle, produce an abbreviated report confirming stability rather than forcing findings that are not there.
- If threat assessment identifies conflicting signals, present both interpretations with the evidence for each rather than forcing a single conclusion.
- If the monitoring cadence is too frequent for the rate of competitive change, recommend adjusting to a longer interval.
- If a new competitor emerges mid-cycle, trigger a full competitor audit (Stage 1) before incorporating them into the comparison stages.

## Cadence Recommendations

| Competitive intensity | Recommended cadence | Report depth |
|----------------------|--------------------|--------------|
| High (fast-moving market) | Weekly | Signal alerts + brief summary |
| Medium (steady competition) | Fortnightly | Full monitoring report |
| Low (stable market) | Monthly | Detailed report with trend analysis |

## Inputs

| Name | Required | Description | Example |
|------|----------|-------------|---------|
| `{{input.competitor_name}}` | Yes | Competitor name | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.website_url}}` | Yes | website URL | `https://example.com/reference` |
| `{{input.known_social_media_profiles}}` | Yes | known social media profiles | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.your_company}}` | Yes | Your company name | `Acme Corp` |
| `{{input.market_segment}}` | Yes | Industry or market segment | `B2B SaaS project management` |
| `{{input.your_positioning}}` | Yes | Your company's current positioning and messaging | `Paste a short summary of your current positioning statement and key messages.` |
| `{{input.any_previous_audit_data}}` | No | any previous audit data | `Paste the latest metrics, exported data, or summary notes relevant to the workflow.` |

## Outputs

| Name | Description |
|------|-------------|
| Structured competitor profile covering all marketing channels, messaging themes, and current positioning | Structured competitor profile covering all marketing channels, messaging themes, and current positioning |
| Messaging comparison matrix showing how each competitor positions themselves, their key differentiators, and messaging gaps or overlaps | Messaging comparison matrix showing how each competitor positions themselves, their key differentiators, and messaging gaps or overlaps |
| Campaign analysis reports and market signal alerts for notable competitive moves | Campaign analysis reports and market signal alerts for notable competitive moves |
| Threat assessment | Threat assessment with prioritised response recommendations |
| Complete competitive monitoring report ready for distribution to stakeholders | Complete competitive monitoring report ready for distribution to stakeholders |

## Setup

Before running this workflow:

1. No external services required — paste your content directly and provide any supporting context as inputs or source nodes.
2. Review the included documents, assets, or source nodes and customise them to match your team, brand, or domain conventions where needed.
3. No specific AI provider or API key is required beyond your configured skrptiq LLM provider.

## Provider Notes

- Most stages work with any capable model; stronger models usually improve synthesis, judgement, and writing quality.
- Extraction, classification, and formatting steps generally run well on smaller or faster models.
- Because there are no vendor-specific integrations here, provider choice is mostly a trade-off between speed, quality, and cost.

## Example Input

To test this workflow immediately after import:

```
Competitor Name: "Paste the relevant brief, notes, source material, or dataset here."
Website Url: "https://example.com/reference"
Known Social Media Profiles: "Paste the relevant brief, notes, source material, or dataset here."
Your Company: "Acme Corp"
Market Segment: "B2B SaaS project management"
Your Positioning: "Paste a short summary of your current positioning statement and key messages."
Any Previous Audit Data: "Paste the latest metrics, exported data, or summary notes relevant to the workflow."
```

