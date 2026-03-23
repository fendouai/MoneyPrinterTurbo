---
name: video-speech-director
description: Direct the speech synthesis to achieve natural, engaging delivery. Controls pace, emphasis, pauses, and emotional expression.
---

# Video Speech Director

## Core Job

Use this skill to **direct the voice synthesis** for optimal delivery quality.

This layer owns:

- speech rate optimization
- emphasis placement
- pause design
- emotional expression
- naturalness enhancement

## Speech Parameters

### 1. Speech Rate
| Rate | Speed | Use Case |
|------|-------|----------|
| 0.7 | Very slow | Dramatic, emphasis |
| 0.8-0.9 | Slow | Emotional, serious |
| 1.0 | Normal | Educational, informative |
| 1.1-1.2 | Slightly fast | Energetic, engaging |
| 1.3+ | Fast | Urgent, exciting |

### 2. Volume
| Volume | Use Case |
|--------|----------|
| 0.8 | Background elements |
| 1.0 | Normal speech |
| 1.2 | Emphasis moments |

### 3. Pause Types
- **Breath pause**: Natural breathing (0.3-0.5s)
- **Emphasis pause**: Before key points (0.5-1.0s)
- **Section pause**: Between topics (1.0-2.0s)
- **Dramatic pause**: For impact (1.5-2.0s)

## Workflow

### 1. Script Segmentation
Break script into logical speech units.

### 2. Emphasis Mapping
Identify words/phrases for emphasis.

### 3. Pause Design
Plan pauses for natural flow.

### 4. Emotional Variation
Map emotional tone to speech sections.

### 5. Synthesis Direction
Guide TTS parameters for each section.

## Input Contract

```yaml
script: object
selected_voice: object
delivery_guidance: object
```

## Output Contract

```yaml
speech_direction:
  global_settings:
    voice_name: "zh-CN-XiaoxiaoNeural"
    base_rate: 1.0
    base_volume: 1.0
    
  script_segmentation:
    - id: 1
      text: "你有没有发现"
      type: "hook"
      rate: 1.0
      emphasis: ["发现"]
      pause_after: 0.3
      
    - id: 2
      text: "越是忙碌的人，反而越有时间"
      type: "hook_continuation"
      rate: 0.95
      emphasis: ["反而"]
      pause_after: 0.5
      
    - id: 3
      text: "每天都在忙，但回头一看，好像什么都没做成"
      type: "problem"
      rate: 1.0
      emphasis: ["什么都没做成"]
      pause_after: 0.8
      
    - id: 4
      text: "真相是"
      type: "insight_intro"
      rate: 0.85
      emphasis: ["真相"]
      pause_after: 0.5
      
    - id: 5
      text: "时间从来不是问题。问题是你把注意力都花在了哪儿"
      type: "insight"
      rate: 0.95
      emphasis: ["从来不是", "注意力"]
      pause_after: 1.0
      
  emotional_markers:
    - position: "hook"
      emotion: "curious"
      expression: "slightly questioning tone"
      
    - position: "problem"
      emotion: "relatable frustration"
      expression: "empathetic tone"
      
    - position: "insight"
      emotion: "enlightenment"
      expression: "clearer, more confident"
      
    - position: "landing"
      emotion: "empowerment"
      expression: "warm, encouraging"
      
  pause_schedule:
    - position: "after hook"
      duration: 0.5
      type: "section"
      reason: "Let hook land"
      
    - position: "before '真相是'"
      duration: 0.8
      type: "emphasis"
      reason: "Build anticipation"
      
    - position: "after key insight"
      duration: 1.0
      type: "dramatic"
      reason: "Let insight sink in"
      
  synthesis_parameters:
    total_estimated_duration: 45
    average_rate: 0.98
    naturalness_priority: "high"
    
  quality_targets:
    naturalness: 8
    clarity: 9
    emotional_expression: 8
    engagement: 9