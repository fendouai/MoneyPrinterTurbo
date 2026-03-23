---
name: video-script-reviewer
description: Review and critique video script for quality, engagement, and platform suitability. Identifies issues before production.
---

# Video Script Reviewer

## Core Job

Use this skill to **evaluate script quality** before moving to production.

This layer owns:

- quality assessment
- engagement prediction
- issue identification
- improvement recommendations
- version comparison

## Review Dimensions

### 1. Hook Strength (Critical)
- Pattern interrupt score (1-10)
- Curiosity gap score (1-10)
- First-3-second engagement prediction

### 2. Content Quality
- Value density
- Information accuracy
- Logical flow
- Emotional arc

### 3. Platform Fit
- Duration appropriateness
- Platform-specific elements
- Algorithm optimization

### 4. Engagement Predictors
- Re-watchability
- Shareability
- Comment-worthiness
- Save-worthiness

### 5. Production Readiness
- Clarity for voice talent
- Timing accuracy
- Technical feasibility

## Review Criteria

| Dimension | Weight | Must Pass |
|-----------|--------|-----------|
| Hook Strength | 30% | Score ≥ 7 |
| Content Quality | 25% | No blocking issues |
| Platform Fit | 20% | Duration within target |
| Engagement | 15% | Predicted engagement ≥ medium |
| Production Ready | 10% | All clear |

## Workflow

### 1. Hook Review
- First 3 seconds analysis
- Pattern interrupt evaluation
- Curiosity gap assessment

### 2. Content Review
- Value delivery check
- Logical flow analysis
- Golden line identification

### 3. Platform Review
- Duration match
- Platform requirements
- Algorithm factors

### 4. Engagement Prediction
- Likely audience reaction
- Viral potential assessment
- Interaction triggers

### 5. Issue Identification
- Blocking issues (must fix)
- Improvement opportunities
- Polish suggestions

## Input Contract

```yaml
script: object
topic_analysis: object
platform: string
```

## Output Contract

```yaml
review:
  overall_score:
  pass_fail:
  
  dimension_scores:
    hook_strength: 8
    content_quality: 7
    platform_fit: 9
    engagement: 8
    production_ready: 10
    
  hook_assessment:
    pattern_interrupt: 8
    curiosity_gap: 9
    first_3_seconds: "Strong question hook with relatable premise"
    
  content_assessment:
    value_density: "High - every sentence adds value"
    logical_flow: "Clear problem → insight → solution structure"
    golden_lines: 2
    weak_points: []
    
  engagement_prediction:
    re_watchability: "Medium - insight worth revisiting"
    shareability: "High - quotable and relatable"
    comment_worthy: "High - invites discussion"
    save_worthy: "Medium - practical value"
    predicted_engagement: "medium-high"
    
  issues:
    blocking:
      - issue: null
        fix: null
        
    improvements:
      - issue: "Middle section slightly long"
        suggestion: "Consider trimming 2-3 seconds"
        impact: "Better pacing"
        
    polish:
      - suggestion: "Consider stronger ending CTA"
        impact: "Higher conversion"
        
  final_recommendation:
    status: "approved"  # approved, needs_revision, rejected
    notes:
    required_changes:
```

## Decision Matrix

| Score | Status | Action |
|-------|--------|--------|
| 8-10 | Approved | Proceed to production |
| 6-7 | Needs Revision | Fix blocking issues |
| Below 6 | Rejected | Major rewrite needed |