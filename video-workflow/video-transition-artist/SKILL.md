---
name: video-transition-artist
description: Design and apply transitions between clips that enhance storytelling and maintain viewer engagement.
---

# Video Transition Artist

## Core Job

Use this skill to **design transitions** that enhance the viewing experience.

This layer owns:

- transition selection
- transition timing
- visual continuity
- storytelling enhancement
- style consistency

## Transition Types

### 1. Hard Cut
- Instant change
- Use: Fast-paced, documentary
- Impact: Neutral, invisible

### 2. Dissolve/Crossfade
- Gradual blend
- Use: Emotional, passage of time
- Impact: Soft, reflective

### 3. Fade to Black/White
- Transition to/from black/white
- Use: Scene endings, dramatic
- Impact: Finality, emphasis

### 4. Wipe
- One image replaces another
- Use: Dynamic, stylized
- Impact: Energetic, directional

### 5. Zoom Transitions
- Zoom in/out to next clip
- Use: Tech, modern
- Impact: Dynamic, attention-grabbing

### 6. Match Cut
- Visual continuity across clips
- Use: Sophisticated, cinematic
- Impact: Seamless, artistic

## Transition Selection Guide

| Content Type | Primary Transition | Secondary |
|--------------|-------------------|-----------|
| Educational | Hard cut | Fade |
| Emotional | Dissolve | Fade |
| Action | Hard cut | Wipe |
| Documentary | Hard cut | Dissolve |
| Promotional | Mix | Zoom |

## Workflow

### 1. Analyze Content Flow
Understand narrative structure.

### 2. Select Transition Types
Match to content and mood.

### 3. Time Transitions
Determine duration for each.

### 4. Ensure Consistency
Maintain style throughout.

### 5. Quality Check
Verify smooth playback.

## Input Contract

```yaml
timing_plan: object
mood_direction: object
transition_preferences: object
```

## Output Contract

```yaml
transition_design:
  style_direction:
    primary_style: "minimal"
    consistency: "high"
    avoid_overuse: true
    
  transition_sequence:
    - from_clip: "scene_1"
      to_clip: "scene_2"
      transition_type: "hard_cut"
      duration: 0
      rationale: "Maintain energy in hook section"
      
    - from_clip: "scene_2"
      to_clip: "scene_3"
      transition_type: "dissolve"
      duration: 0.5
      rationale: "Transition to insight, emotional shift"
      
    - from_clip: "scene_3"
      to_clip: "scene_4"
      transition_type: "hard_cut"
      duration: 0
      rationale: "Keep momentum"
      
    - from_clip: "scene_4"
      to_clip: "scene_5"
      transition_type: "dissolve"
      duration: 0.3
      rationale: "Gentle transition to landing"
      
  special_transitions:
    - position: "insight_reveal"
      type: "slow_dissolve"
      duration: 0.8
      purpose: "Emphasize key moment"
      
  transition_count:
    total: 7
    hard_cuts: 4
    dissolves: 3
    special: 1
    
  timing_adjustments:
    "scene_2_to_3": "Add 0.2s to dissolve for better flow"
    
  quality_metrics:
    visual_continuity: 8
    rhythm_consistency: 9
    style_alignment: 9