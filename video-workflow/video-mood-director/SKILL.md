---
name: video-mood-director
description: Define the emotional tone and visual atmosphere for the video. Creates mood boards and visual direction guides.
---

# Video Mood Director

## Core Job

Use this skill to **define the emotional and atmospheric direction** for all visual elements.

This layer owns:

- mood definition
- color psychology
- visual atmosphere
- emotional pacing
- mood board creation

## Mood Categories

### 1. Energy Level
- High Energy: Bright, fast, dynamic
- Medium Energy: Balanced, steady
- Low Energy: Calm, reflective, slow

### 2. Emotional Tone
- Inspiring: Uplifting, motivational
- Educational: Clear, trustworthy
- Dramatic: Intense, emotional
- Playful: Fun, lighthearted
- Serious: Professional, authoritative

### 3. Visual Atmosphere
- Warm: Orange, yellow, comfortable
- Cool: Blue, teal, professional
- Neutral: Gray, white, clean
- Vibrant: Saturated, colorful
- Muted: Desaturated, subtle

## Color Psychology

| Color | Emotion | Use Case |
|-------|---------|----------|
| Blue | Trust, calm | Business, education |
| Orange | Energy, warmth | Lifestyle, motivation |
| Green | Growth, nature | Health, finance |
| Red | Urgency, passion | Alerts, excitement |
| Yellow | Optimism, clarity | Happiness, creativity |
| Purple | Luxury, wisdom | Premium, innovative |
| Black | Sophistication, power | Luxury, tech |

## Workflow

### 1. Analyze Emotional Journey

Map emotions across script:
```
Start: Curious, questioning
Middle: Insight, realization
End: Empowered, motivated
```

### 2. Define Color Direction

Primary and secondary colors:
- Main color palette
- Accent colors
- Color transitions

### 3. Create Mood Reference

Visual references for:
- Color treatment
- Lighting style
- Composition style
- Texture/feel

### 4. Guide Consistency

Ensure all visuals align with mood:
- Temperature consistency
- Style uniformity
- Emotional coherence

## Input Contract

```yaml
visual_plan: object
topic_analysis: object
script: object
```

## Output Contract

```yaml
mood_direction:
  primary_mood: "inspiring"
  energy_level: "medium"
  emotional_journey:
    - timestamp: "0-10s"
      mood: "curious, questioning"
      visual_tone: "slightly tense"
    - timestamp: "10-25s"
      mood: "insight, realization"
      visual_tone: "brightening"
    - timestamp: "25-45s"
      mood: "empowered, motivated"
      visual_tone: "confident, warm"
      
  color_direction:
    primary_palette:
      - color: "#2C3E50"
        usage: "Shadows, depth"
      - color: "#E67E22"
        usage: "Warmth, energy accent"
      - color: "#ECF0F1"
        usage: "Highlights, clarity"
    secondary_palette:
      - color: "#3498DB"
        usage: "Trust, calm moments"
    color_temperature: "warm-neutral"
    saturation_level: "medium"
    
  lighting_direction:
    style: "natural, soft"
    key_light: "Diffused daylight"
    contrast: "medium"
    shadow_handling: "soft, not harsh"
    
  composition_style:
    framing: "center-weighted for mobile"
    depth_preference: "shallow depth of field"
    movement: "steady, minimal shake"
    rule_of_thirds: "less important for vertical"
    
  visual_texture:
    overall_feel: "clean, modern, authentic"
    grain: "minimal"
    sharpness: "high"
    
  mood_board_references:
    - description: "Modern professional, natural lighting"
      keywords: ["corporate lifestyle", "modern office", "natural light"]
    - description: "Moment of clarity"
      keywords: ["sunlight", "peaceful", "contemplative"]
      
  dos:
    - "Use natural, authentic imagery"
    - "Maintain warm, inviting tones"
    - "Keep compositions clean and focused"
    
  donts:
    - "Avoid harsh, cold lighting"
    - "No overly dramatic or staged shots"
    - "Stay away from cluttered compositions"