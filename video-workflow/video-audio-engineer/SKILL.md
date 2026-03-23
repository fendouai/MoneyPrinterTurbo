---
name: video-audio-engineer
description: Execute the audio synthesis and mixing. Produces final audio file with voice, music, and sound effects properly mixed.
---

# Video Audio Engineer

## Core Job

Use this skill to **execute audio production** - synthesizing voice and mixing all audio elements.

This layer owns:

- voice synthesis execution
- audio mixing
- volume balancing
- audio quality control
- final audio export

## Audio Specifications

### Export Settings
- Format: MP3 (192kbps) or WAV (for quality)
- Sample Rate: 44100 Hz
- Channels: Stereo
- Bit Depth: 16-bit (WAV)

### Volume Standards
| Element | Level |
|---------|-------|
| Voice | -6 to -3 dB |
| Music | -18 to -12 dB |
| SFX | -12 to -6 dB |
| Master | -3 to -1 dB peak |

## Workflow

### 1. Voice Synthesis
Execute TTS with directed parameters.

### 2. Audio Preparation
- Normalize voice audio
- Prepare music track
- Load sound effects

### 3. Mixing
- Balance voice and music
- Apply volume automation
- Add sound effects

### 4. Mastering
- Final EQ adjustments
- Compression if needed
- Limiter for peak control

### 5. Export
Generate final audio file.

## Input Contract

```yaml
script: object
speech_direction: object
sound_design: object
output_path: string
```

## Output Contract

```yaml
audio_production:
  voice_synthesis:
    file: "work/videos/task/audio.mp3"
    voice: "zh-CN-XiaoxiaoNeural"
    duration: 42.5
    sample_rate: 44100
    status: "complete"
    quality_check:
      clarity: "good"
      naturalness: "good"
      issues: []
    
  audio_mix:
    voice_track: "audio.mp3"
    music_track: "inspiring-corporate.mp3"
    sfx_tracks:
      - "whoosh_01.wav"
      - "ding_subtle.wav"
      
    mix_settings:
      voice_level: 0
      music_level: -15
      ducking_enabled: true
      ducking_threshold: -20
      
  final_audio:
    file: "work/videos/task/final_audio.mp3"
    duration: 42.5
    format: "MP3"
    bitrate: 192
    sample_rate: 44100
    channels: 2
    peak_level: -2.3
    rms_level: -14.5
    
  quality_metrics:
    voice_clarity: 9
    music_balance: 8
    overall_mix: 8
    loudness_standard: "passes"
    
  production_notes:
    - "Applied slight compression to voice for consistency"
    - "Music ducked during key phrases"
    - "Added subtle fade out at end"