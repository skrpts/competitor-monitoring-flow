---
type: skill
id: messaging-comparison
title: Messaging Comparison Matrix
description: "Building a side-by-side comparison of messaging, positioning, and value propositions across all tracked competitors"
tags: [Production, Competitive, Metrics]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "3-5 minutes"
  avg_tokens: 2500
  trigger: manual
---

## Messaging Comparison Matrix

This skill builds a structured, side-by-side comparison of how each tracked competitor positions itself, drawing on the messaging analysis produced upstream.

### Core Capability

Given the competitor audit and messaging analysis, this skill maps every competitor (and your own company) across positioning dimensions — tagline, category claim, target audience, primary value proposition, key differentiator, proof points, pricing position, and emotional appeal — then surfaces the patterns: contested pillars, unclaimed territory, and messaging vulnerabilities.

### Method

1. **Positioning table:** Compare each competitor across the core positioning dimensions, one row per dimension, one column per player.
2. **Pillar analysis:** Identify each competitor's 3-5 messaging pillars and map overlap — unique, contested, owned, and unclaimed themes.
3. **Gap analysis:** Surface themes no competitor addresses, overused claims, and audience segments underserved by current messaging.

### Output Structure

A set of clean comparison tables followed by messaging recommendations and a short executive summary. The matrix feeds the threat assessment and monitoring report stages downstream.
