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
  - target: claude-service
    type: runs_on
  - target: competitive-marketing-framework
    type: references
  - target: competitor-monitoring-playbook
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

Invoke the **competitor-audit-prompt** to produce a comprehensive baseline audit of each competitor's marketing presence. This covers their website messaging, content strategy, social media activity, advertising presence, and market positioning.

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
| Low (stable market) | Monthly | Comprehensive report with trend analysis |
