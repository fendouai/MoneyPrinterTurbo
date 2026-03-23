---
name: video-visual-planner
description: Plan visual requirements for the video. Identifies needed visual elements, styles, and transitions based on script content and emotional journey.
---

# Video Visual Planner

## Core Job

Use this skill to **plan all visual elements** needed for the video before sourcing.

This layer owns:

- visual requirements analysis
- scene breakdown
- visual style direction
- transition planning
- visual-emotional mapping

## Workflow

### 1. Script Visual Analysis

Break down script into visual segments:

```
Section 1 (Hook): "你有没有发现，越是忙碌的人，反而越有时间？"
- Visual need: Relatable busy person scene
- Mood: Curious, relatable
- Keywords: busy, office worker, multitasking

Section 2 (Problem): "每天都在忙，但回头一看..."
- Visual need: Overwhelmed feeling, scattered tasks
- Mood: Recognizing the problem
- Keywords: stressed, overwhelmed, tired
```

### 2. Visual Style Direction

Define the visual language:

| Style | Characteristics | Use Case |
|-------|-----------------|----------|
| Cinematic | High production, dramatic | Emotional, premium |
| Documentary | Natural, authentic | Educational, serious |
| Minimalist | Clean, simple | Tech, modern |
| Vibrant | Colorful, energetic | Lifestyle, youth |
| Moody | Dark, atmospheric | Drama, emotion |

### 3. Scene Requirements

For each script section:
- Subject/Action needed
- Environment/Setting
- Emotional tone
- Visual metaphor options

### 4. Transition Planning

Plan how visuals flow:
- Cut rhythm
- Transition types
- Emotional continuity

## Input Contract

```yaml
script: object
topic_analysis: object
architecture: object
```

## Output Contract

```yaml
visual_plan:
  style_direction:
    primary_style: "documentary"
    secondary_style: "cinematic"
    color_palette: "warm, natural"
    mood_keywords: ["authentic", "relatable", "inspiring"]
    
  scene_breakdown:
    - section: "hook"
      timestamp: "0-3s"
      script_text: "你有没有发现..."
      visual_requirement: "Busy professional in modern office"
      visual_keywords: ["busy person", "office work", "professional"]
      mood: "curious, relatable"
      metaphor_options: ["clock close-up", "rushing person"]
      
    - section: "problem"
      timestamp: "3-10s"
      script_text: "每天都在忙..."
      visual_requirement: "Overwhelmed feeling, scattered tasks"
      visual_keywords: ["stressed", "overwhelmed", "tired worker"]
      mood: "recognition, tension"
      metaphor_options: ["clock ticking", "piles of paper"]
      
    - section: "insight"
      timestamp: "10-25s"
      script_text: "真相是..."
      visual_requirement: "Moment of clarity, focus"
      visual_keywords: ["focused", "clarity", "calm working"]
      mood: "enlightenment"
      metaphor_options: ["sunlight", "clear desk", "focused eyes"]
      
    - section: "solution"
      timestamp: "25-40s"
      script_text: "真正高效的人..."
      visual_requirement: "Productive, intentional work"
      visual_keywords: ["productive", "efficient", "success"]
      mood: "empowerment"
      metaphor_options: ["checklist completion", "satisfied smile"]
      
    - section: "landing"
      timestamp: "40-45s"
      script_text: "记住..."
      visual_requirement: "Confident, reflective moment"
      visual_keywords: ["confident", "reflection", "success"]
      mood: "motivation"
      metaphor_options: ["sunrise", "walking forward"]

  transition_plan:
    - from: "hook"
      to: "problem"
      type: "hard cut"
      reason: "Maintain tension"
      
    - from: "problem"
      to: "insight"
      type: "fade"
      reason: "Transition to positive tone"
      
  total_clips_needed: 8
  total_duration: 45
  
  sourcing_notes:
    priority_sources: ["pexels", "pixabay"]
    license_requirements: "Free for commercial use"
    aspect_ratio: "9:16"