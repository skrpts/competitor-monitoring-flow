---
type: skill
id: monitoring-report
title: Monitoring Report Writer
description: "Compiling a periodic competitive monitoring report from the messaging matrix, threat assessment, and market signals"
tags: [Production, Competitive, Metrics]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "5-8 minutes"
  avg_tokens: 3500
  trigger: manual
---

## Monitoring Report Writer

This skill assembles the deliverable of the workflow: a concise, actionable periodic monitoring report for marketing leadership, focused on what has changed since the last cycle.

### Core Capability

Given the messaging comparison matrix, the threat assessment, and the market signals as inputs, this skill compiles a structured report covering the competitive landscape status, per-competitor updates, market signals and trends, a threat and opportunity register, prioritised recommended actions, and a forward look.

### Method

1. **Synthesis:** Draw the executive summary from the threat assessment and messaging matrix, distilling the single most significant development and top recommended action.
2. **Structured sections:** Populate competitor status updates, market signals, the threat/opportunity register, and recommended actions (immediate, near-term, ongoing) from the upstream artifacts.
3. **Signal over noise:** Keep the report to 2-4 pages, ensuring every finding connects to a recommended action or a monitoring adjustment.

### Output Structure

A complete monitoring report following the monitoring-report-template format, ready for distribution to stakeholders. This is the final content artifact before language polishing.
