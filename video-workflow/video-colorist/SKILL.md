---
name: video-colorist
description: Apply color grading and visual treatment to ensure consistent look and enhance mood across all clips.
---

# Video Colorist

## Core Job

Use this skill to **ensure visual consistency** through color grading and treatment.

This layer owns:

- color grading
- look consistency
- mood enhancement
- visual polish
- style application

## Color Grading Basics

### 1. Color Correction
- White balance adjustment
- Exposure correction
- Color consistency across clips

### 2. Color Grading (Creative)
- Mood enhancement
- Style application
- Visual storytelling

### 3. Common Looks
| Look | Characteristics | Use Case |
|------|-----------------|----------|
| Natural | True-to-life colors | Documentary |
| Warm | Orange/yellow tint | Lifestyle, friendly |
| Cool | Blue/teal tint | Professional, tech |
| Cinematic | Contrast, muted colors | Drama |
| Vintage | Desaturated, warm | Nostalgia |
| High-key | Bright, minimal shadows | Optimistic |
| Low-key | Dark, moody | Dramatic |

## Workflow

### 1. Analyze Source Material
Identify color variations and issues.

### 2. Define Target Look
Match to mood direction.

### 3. Correction Pass
Fix technical issues.

### 4. Grading Pass
Apply creative look.

### 5. Consistency Check
Ensure all clips match.

## Input Contract

```yaml
curated_selection: object
mood_direction: object
color_preferences: object
```

## Output Contract

```yaml
color_grading:
  analysis:
    source_variation: "moderate"
    issues_found:
      - "Clip 3 slightly cooler than others"
      - "Clip 5 has slight green cast"
      
  target_look:
    style: "warm_natural"
    description: "Warm, inviting, professional"
    reference: "Modern lifestyle content"
    
  corrections:
    - clip: "scene_1"
      white_balance: "neutral"
      exposure: "+0.1"
      contrast: "0"
      notes: "Good as-is"
      
    - clip: "scene_2"
      white_balance: "+200K"
      exposure: "0"
      contrast: "+5%"
      notes: "Warmed up slightly"
      
    - clip: "scene_3"
      white_balance: "+300K"
      exposure: "+0.2"
      contrast: "+3%"
      saturation: "-5%"
      notes: "Matched to warm look"
      
  grading:
    primary_adjustments:
      shadows: "slight warm tint"
      midtones: "neutral"
      highlights: "warm lift"
    saturation: "-5%"
    vibrance: "+5%"
    contrast_curve: "gentle S-curve"
    
  lut_settings:
    name: "warm_natural_v1"
    intensity: 80
    
  consistency_metrics:
    color_match: 9
    exposure_match: 9
    overall_consistency: 9
    
  export_settings:
    color_space: "Rec.709"
    bit_depth: "8-bit"
    gamma: "2.4"