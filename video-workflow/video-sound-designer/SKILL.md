---
name: video-sound-designer
description: Design background music and sound effects that enhance the video without overpowering the narration.
---

# Video Sound Designer

## Core Job

Use this skill to **design the audio atmosphere** with music and sound effects.

This layer owns:

- background music selection
- sound effect design
- audio atmosphere creation
- music-video sync
- audio branding

## Music Categories

### By Mood
| Mood | Characteristics | Use Case |
|------|-----------------|----------|
| Uplifting | Major key, bright | Motivational |
| Calm | Slow, peaceful | Educational |
| Dramatic | Tension, dynamics | Storytelling |
| Energetic | Fast, driving | Action |
| Emotional | Piano, strings | Touching moments |

### By Genre
| Genre | Feel | Platform Fit |
|-------|------|--------------|
| Lo-fi | Relaxed, modern | Lifestyle |
| Corporate | Professional | Business |
| Cinematic | Epic, emotional | Documentary |
| Electronic | Modern, tech | Tech content |
| Acoustic | Natural, warm | Personal |

## Music Selection Criteria

### 1. Tempo Match
- Match or slightly under speech pace
- Avoid conflicting rhythms

### 2. Key & Mood Match
- Major for positive/inspiring
- Minor for emotional/dramatic

### 3. Instrumentation
- Avoid heavy bass that conflicts with voice
- Prefer non-vocal tracks
- Piano/guitar work well with speech

### 4. Structure
- Need sections that can loop
- Avoid strong drops that distract
- Consistent energy level

## Workflow

### 1. Analyze Content Mood
Determine emotional atmosphere needed.

### 2. Select Music Style
Match to content type and tone.

### 3. Choose Specific Tracks
Select from available library.

### 4. Plan Music Sync
Map music to video sections.

### 5. Design SFX (if needed)
Add sound effects for impact.

## Input Contract

```yaml
script: object
mood_direction: object
speech_direction: object
audio_duration: float
music_preferences:
  style: string        # optional
  mood: string         # optional
```

## Output Contract

```yaml
sound_design:
  music_selection:
    primary_track:
      name: "inspiring-corporate"
      file: "resource/songs/inspiring-corporate.mp3"
      duration: 120
      tempo: 95
      key: "C Major"
      mood: "uplifting, professional"
      instrumentation: ["piano", "light strings", "subtle drums"]
      energy_level: "medium"
      loop_friendly: true
      
    backup_track:
      name: "warm-motivation"
      file: "resource/songs/warm-motivation.mp3"
      duration: 90
      mood: "warm, encouraging"
      
  music_sync_plan:
    intro:
      start: 0
      end: 10
      volume: 0.15
      note: "Subtle entry, not competing with hook"
      
    body:
      start: 10
      end: 35
      volume: 0.12
      note: "Lower volume for clarity"
      
    climax:
      start: 35
      end: 40
      volume: 0.18
      note: "Slight swell for key insight"
      
    landing:
      start: 40
      end: 45
      volume: 0.10
      note: "Fade under CTA"
      
  volume_automation:
    - position: 0
      volume: 0.15
    - position: 10
      volume: 0.12
    - position: 35
      volume: 0.18
    - position: 42
      volume: 0.10
    - position: 45
      volume: 0.0
      
  sound_effects:
    - type: "whoosh"
      position: 3.5
      purpose: "Transition after hook"
      volume: 0.3
    - type: "subtle_ding"
      position: 28
      purpose: "Emphasize key insight"
      volume: 0.2
      
  audio_mix:
    voice_volume: 1.0
    music_volume: 0.15
    sfx_volume: 0.25
    master_headroom: -3dB
    
  licensing:
    all_tracks: "royalty-free for commercial use"
    attribution_required: false