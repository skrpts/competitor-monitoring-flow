---
type: skill
id: threat-assessment
title: Threat Assessment
description: "Assessing competitive threats by severity and urgency and recommending prioritised defensive and offensive responses"
tags: [Production, Competitive, Metrics]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "3-5 minutes"
  avg_tokens: 2500
  trigger: manual
---

## Threat Assessment

This skill evaluates the competitive threats surfaced through monitoring and turns them into a prioritised, actionable response plan.

### Core Capability

Given the messaging analysis and campaign tracking data as the evidence base, this skill identifies and classifies each competitive threat by severity, urgency, and confidence, analyses the impact of the most serious ones, and recommends specific defensive and offensive responses.

### Method

1. **Threat classification:** Catalogue each signal or pattern with a severity, urgency, confidence, and source, applying explicit severity criteria from critical down to low.
2. **Impact analysis:** For high-severity and critical threats, assess customers at risk, revenue and positioning impact, timeline, and compounding risk.
3. **Response planning:** Recommend defensive actions (messaging reinforcement, retention, sales enablement) and offensive opportunities (counter-positioning, market gaps, timing windows), then produce a prioritised action plan.

### Output Structure

An executive summary stating the overall threat level and single most important action, followed by the classified threat register, impact analysis, and prioritised action plan. The assessment feeds the monitoring report stage downstream.
