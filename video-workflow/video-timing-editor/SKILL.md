---
name: video-timing-editor
description: Fine-tune the timing and pacing of video clips to match audio and create optimal rhythm.
---

# Video Timing Editor

## Core Job

Use this skill to **perfect the timing and rhythm** of video clips in relation to audio.

This layer owns:

- clip timing optimization
- rhythm creation
- audio-video sync
- pace variation
- breathing room design

## Timing Principles

### 1. Audio-Visual Sync
- Clip changes on audio beats
- Match visual energy to audio energy
- Avoid awkward mismatches

### 2. Pacing Patterns
| Pattern | Description | Use Case |
|---------|-------------|----------|
| Steady | Consistent 3-5s clips | Educational |
| Accelerating | Gradually shorter clips | Building tension |
| Dynamic | Varies with content | Storytelling |
| Punchy | Quick 1-2s cuts | High energy |

### 3. Cognitive Load
- Allow time to process visuals
- Match complexity to duration
- Avoid over-stimulation

## Workflow

### 1. Analyze Audio Structure
Identify audio sections, beats, and emphasis points.

### 2. Map Visual Cuts
Align clip changes with audio.

### 3. Fine-tune Durations
Adjust for optimal rhythm.

### 4. Add Breathing Room
Ensure viewer can process content.

### 5. Sync Check
Verify audio-visual alignment.

## Input Contract

```yaml
curated_selection: object
speech_direction: object
audio_production: object
```

## Output Contract

```yaml
timing_plan:
  audio_structure:
    total_duration: 42.5
    sections:
      - name: "hook"
        start: 0
        end: 3
        energy: "medium"
      - name: "problem"
        start: 3
        end: 12
        energy: "medium-high"
      - name: "insight"
        start: 12
        end: 30
        energy: "high"
      - name: "solution"
        start: 30
        end: 38
        energy: "medium-high"
      - name: "landing"
        start: 38
        end: 42.5
        energy: "medium"
        
  visual_timing:
    - clip_id: "scene_1"
      source: "pexels_12345"
      start: 0.0
      end: 3.5
      duration: 3.5
      transition_in: "none"
      transition_out: "cut"
      sync_point: "on hook completion"
      
    - clip_id: "scene_2"
      source: "pixabay_67890"
      start: 3.5
      end: 8.0
      duration: 4.5
      transition_in: "cut"
      transition_out: "cut"
      sync_point: "on problem phrase"
      
    - clip_id: "scene_3"
      source: "pexels_23456"
      start: 8.0
      end: 15.0
      duration: 7.0
      transition_in: "fade 0.3s"
      transition_out: "cut"
      sync_point: "on insight reveal"
      
  pacing_profile:
    pattern: "dynamic"
    average_clip_duration: 5.3
    shortest_clip: 3.0
    longest_clip: 7.0
    cut_frequency: "moderate"
    
  emphasis_points:
    - time: 12.5
      type: "insight reveal"
      action: "hold clip, slight slow-mo"
    - time: 38.0
      type: "key takeaway"
      action: "slower pace, emphasize"
      
  breathing_room:
    - position: "after hook"
      duration: 0.3
      purpose: "let hook land"
    - position: "after key insight"
      duration: 0.5
      purpose: "allow processing"
      
  sync_verification:
    audio_video_aligned: true
    cut_points_on_beat: true
    emphasis_synced: true