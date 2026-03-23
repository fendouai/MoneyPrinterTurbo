---
name: video-subtitle-stylist
description: Design and apply subtitle styling that is readable, on-brand, and enhances comprehension without distracting from content.
---

# Video Subtitle Stylist

## Core Job

Use this skill to **design and apply subtitle styling** for optimal readability and aesthetics.

This layer owns:

- subtitle timing
- font selection
- styling design
- position optimization
- readability assurance

## Subtitle Style Elements

### 1. Font Selection
| Style | Font | Use Case |
|-------|------|----------|
| Modern | STHeitiMedium, PingFang | Contemporary |
| Classic | Songti SC | Traditional, serious |
| Playful | Rounded fonts | Casual, fun |
| Bold | Impact-style | Emphasis |

### 2. Size Guidelines
| Platform | Recommended Size |
|----------|-----------------|
| Mobile (9:16) | 50-70px |
| Desktop (16:9) | 40-60px |
| Stories/Shorts | 60-80px |

### 3. Position Options
- Bottom (default): Safe, standard
- Center: Emphasis, drama
- Dynamic: Moves to avoid visual conflicts

### 4. Color & Effects
| Element | Options |
|---------|---------|
| Text Color | White (#FFFFFF), Yellow (#FFD700) |
| Stroke | Black (#000000), contrasting |
| Shadow | Subtle drop shadow |
| Background | Semi-transparent box |

## Workflow

### 1. Analyze Content
- Reading level
- Key terms to emphasize
- Visual background complexity

### 2. Select Style
Match to brand and content type.

### 3. Configure Parameters
Set font, size, color, position.

### 4. Generate Subtitles
Create SRT with timing.

### 5. Quality Check
Verify readability and timing.

## Input Contract

```yaml
audio_production: object
script: object
style_preferences:
  font_name: string      # optional
  position: string       # optional
  brand_colors: object   # optional
```

## Output Contract

```yaml
subtitle_style:
  font:
    name: "STHeitiMedium.ttc"
    size: 60
    weight: "medium"
    
  colors:
    text: "#FFFFFF"
    stroke: "#000000"
    stroke_width: 2.0
    shadow_color: "rgba(0,0,0,0.5)"
    shadow_offset: [2, 2]
    background: "rgba(0,0,0,0.3)"
    
  position:
    vertical: "bottom"
    horizontal: "center"
    margin_bottom: 80
    safe_area: true
    
  animation:
    entry: "fade 0.2s"
    exit: "fade 0.2s"
    
  subtitle_file:
    path: "work/videos/task/subtitle.srt"
    entries: 12
    
  style_preview:
    sample_text: "你有没有发现"
    applied_style: "White text with black stroke, bottom center"
    
  readability_score: 9
  brand_alignment: "consistent with modern, clean aesthetic"
  
  special_formatting:
    emphasis_words:
      - word: "反而"
        style: "bold, larger"
      - word: "真相"
        style: "bold, yellow highlight"
        
  quality_check:
    contrast_ratio: 7.5
    mobile_readability: "excellent"
    timing_accuracy: "good"