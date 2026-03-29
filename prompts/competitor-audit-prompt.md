---
type: prompt
id: competitor-audit-prompt
title: Competitor Audit Prompt
description: "Produces a thorough audit of a competitor's marketing presence across all channels"
tags: [Production, Competitive, Metrics]
connections:
  - target: messaging-analysis
    type: derived_from
  - target: messaging-comparison-matrix
    type: uses
  - target: competitor-audit-template
    type: references
metadata:
  estimated_duration: "5-8 minutes"
  avg_tokens: 3500
---

You are a competitive intelligence analyst conducting a thorough marketing audit of a competitor. Your audit must be thorough, evidence-based, and structured for easy comparison with other competitor audits.

**Competitor Name:** {{input.competitor_name}}
**Competitor Website:** {{input.website_url}}
**Competitor Social Profiles:** {{input.known_social_media_profiles}}
**Industry/Market Segment:** {{input.market_segment}}
**Your Company Name (for context):** {{input.your_company}}
**Previous Audit Date (if applicable):** Include the date of any previous audit if available from the audit data provided.
**Known Recent Changes:** Note any recent changes observed from the provided audit data or competitor materials.

## Audit Sections

Complete each section with specific observations and evidence. Do not speculate without flagging assumptions.

### 1. Brand & Positioning
- **Tagline/Strapline:** What is their current tagline?
- **Positioning Statement:** How do they position themselves? (category, target audience, key differentiator)
- **Brand Personality:** Describe their brand voice and personality in 3-5 adjectives with examples
- **Visual Identity Notes:** Colour palette, imagery style, design maturity (professional/startup/enterprise)

### 2. Website Analysis
- **Homepage Messaging:** What is the first thing a visitor sees and reads? What is the primary CTA?
- **Product/Service Pages:** How do they describe their offering? What features do they emphasise?
- **Pricing Page:** Pricing model (freemium, tiered, enterprise, usage-based), price points if visible, pricing psychology tactics
- **Social Proof:** Customer logos, testimonials, case studies, review scores, trust badges
- **Content Hub:** Blog topics, publication frequency, content quality, SEO focus
- **Conversion Paths:** How do they move visitors towards conversion? What CTAs are used?

### 3. Content & SEO Strategy
- **Blog/Resource Centre:** Topics covered, publication frequency, content depth, target keywords
- **Gated Content:** Whitepapers, ebooks, webinars — what are they gating and what do they ask for?
- **Video Content:** YouTube presence, video topics, production quality
- **Podcast/Audio:** Any podcast presence or audio content?
- **SEO Indicators:** Apparent target keywords, domain authority signals, backlink strategy indicators

### 4. Social Media Presence
- **Platforms Active On:** List all platforms with follower counts where visible
- **Posting Frequency:** How often do they post on each platform?
- **Content Mix:** What types of content do they share? (promotional, educational, cultural, user-generated)
- **Engagement Levels:** Comment, like, and share patterns (high/medium/low relative to follower count)
- **Paid Social Indicators:** Any visible sponsored content or ad campaigns?

### 5. Advertising & Campaigns
- **Search Ads:** Any visible Google Ads or search advertising?
- **Display/Programmatic:** Banner ads or retargeting observed?
- **Social Ads:** Sponsored posts or social media advertising?
- **Recent Campaigns:** Any notable marketing campaigns or launches in the past 3 months?
- **Campaign Themes:** What themes or messages are they pushing in paid channels?

### 6. Email & Nurture Strategy
- **Newsletter:** Do they have a newsletter? What topics do they cover?
- **Sign-up Incentives:** What do they offer to capture email addresses?
- **Email Frequency:** If known, how often do they email subscribers?

### 7. Strengths & Weaknesses Summary
- **Top 3 Marketing Strengths:** What are they doing well?
- **Top 3 Marketing Weaknesses:** Where are the gaps or vulnerabilities?
- **Opportunities for Us:** Where can we differentiate or outperform?

## Output Format

Use the competitor-audit-template structure. Include specific URLs and evidence for claims. Flag any sections where information is unavailable or assumptions are being made. If a previous audit exists, note what has changed since the last audit.
