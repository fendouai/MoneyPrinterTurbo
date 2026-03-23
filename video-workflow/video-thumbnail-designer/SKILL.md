---
name: video-thumbnail-designer
description: Design compelling thumbnails that increase click-through rate and viewer engagement.
---

# Video Thumbnail Designer

## Core Job

Use this skill to **design effective thumbnails** that increase click-through rate.

This layer owns:

- thumbnail composition
- text overlay
- color contrast
- platform optimization
- A/B testing

## Thumbnail Principles

### 1. Face + Expression
- Human face increases CTR
- Expressive reaction shots
- Direct eye contact

### 2. High Contrast Colors
- Bright, saturated colors
- Clear subject separation
- Avoid muddy tones

### 3. Minimal Text
- 3-5 words max
- Large, readable font
- Bold, contrasting colors

### 4. Pattern Interrupt
- Unexpected elements
- Question or intrigue
- Clear value proposition

## Input Contract

```yaml
video_topic: string
target_platform: string
content_summary: string
```

## Output Contract

```yaml
thumbnail_design:
  primary_thumbnail:
    description: "Close-up of person with surprised expression, text overlay: '时间管理的真相'"
    key_elements:
      - "Surprised/confused expression"
      - "Text: '时间管理'"
      - "Bold colors"
    composition:
      rule_of_thirds: true
      safe_zones: "leaving space for platform UI"
    color_treatment:
      primary: "#FF6B35"
      secondary: "#1A1A2E"
      contrast: "high"
      
  platform_variations:
    douyin:
      text: "时间管理的真相"
      recommended_elements: "Face with reaction"
      
    youtube:
      text: "Why You're Doing Time Management Wrong"
      recommended_elements: "Contrasting colors, person"
      
  technical_specs:
    format: "PNG or JPG"
    min_resolution: "1080x1920"
    aspect_ratio: "9:16"
    file_size_limit: "2MB"