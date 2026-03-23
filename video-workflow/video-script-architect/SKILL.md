---
name: video-script-architect
description: Design the structural blueprint for the video script. Decides pacing, information flow, emotional beats, and engagement patterns. Creates the skeleton before writing.
---

# Video Script Architect

## Core Job

Use this skill to **design the structural blueprint** before any writing begins.

This layer owns:

- structure selection
- pacing design
- information flow
- emotional beats placement
- engagement hooks positioning
- section timing

## Workflow

### 1. Select Structure Template

Choose from proven structures:

#### AIDA (Attention → Interest → Desire → Action)
```
0-3s:  Attention hook
3-15s: Build interest with facts
15-35s: Create desire with benefits
35-45s: Call to action
```

#### PAS (Problem → Agitation → Solution)
```
0-5s:  State the problem
5-20s: Agitate the pain
20-45s: Present the solution
```

#### Story Arc (Setup → Conflict → Resolution)
```
0-10s: Setup the scene
10-30s: Introduce conflict/challenge
30-45s: Resolution and takeaway
```

#### Value Pyramid (Hook → Value → Stack → CTA)
```
0-3s:  Hook
3-15s: First value point
15-30s: Stack more value
30-45s: CTA
```

### 2. Design Pacing

Plan the rhythm:

- Hook timing (first 3 seconds)
- Information density per section
- Breathing room for key points
- Build-up to climax
- Landing the ending

### 3. Map Emotional Beats

Plan emotional journey:

```
Start: [curiosity/relatability]
Peak:  [insight/surprise/delight]
End:   [satisfaction/motivation/inspiration]
```

### 4. Position Engagement Triggers

Strategic placement of:

- Pattern interrupts
- Questions
- Surprises
- Relatable moments
- Call-to-interaction

## Input Contract

```yaml
topic_analysis: object
research_brief: object
duration_target: int      # seconds
```

## Output Contract

```yaml
architecture:
  structure_type:
  total_duration:
  
  sections:
    - name: "hook"
      duration: 3
      purpose: "Grab attention"
      emotional_beat: "curiosity"
      
    - name: "problem_setup"
      duration: 8
      purpose: "Establish relatability"
      emotional_beat: "recognition"
      
    - name: "insight_delivery"
      duration: 20
      purpose: "Deliver core value"
      emotional_beat: "enlightenment"
      
    - name: "landing"
      duration: 10
      purpose: "Drive action"
      emotional_beat: "motivation"

  pacing_notes:
    tension_points:
    breathing_room:
    climax_position:
    
  engagement_triggers:
    - position: 3
      type: "question"
      content: "你有没有发现..."
    - position: 25
      type: "surprise"
      content: "真相是..."
      
  hook_requirements:
    first_3_seconds:
    pattern_interrupt:
    
  ending_requirements:
    takeaway:
    cta_type:
```

## Timing Guidelines

| Duration | Sections | Hook Time | Value Density |
|----------|----------|-----------|---------------|
| 15-30s | 2-3 | 0-2s | High |
| 30-60s | 3-4 | 0-3s | Medium-High |
| 60-120s | 4-5 | 0-3s | Medium |
| 120s+ | 5-7 | 0-5s | Varied |