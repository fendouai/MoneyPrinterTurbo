---
name: video-quality-controller
description: Final quality control before video delivery. Checks technical specs, content accuracy, and overall production quality.
---

# Video Quality Controller

## Core Job

Use this skill to **perform final quality assurance** before video delivery.

This layer owns:

- technical QC
- content accuracy check
- playback verification
- platform compliance
- final approval

## QC Checklist

### 1. Technical Quality
- [ ] Resolution matches target
- [ ] Frame rate correct
- [ ] No visual artifacts
- [ ] Audio sync verified
- [ ] Color accuracy

### 2. Content Quality
- [ ] Script accuracy
- [ ] Subtitle timing
- [ ] Visual relevance
- [ ] Brand compliance

### 3. Platform Compliance
- [ ] Duration within limits
- [ ] Aspect ratio correct
- [ ] File size acceptable
- [ ] Format supported

### 4. Playback Quality
- [ ] Smooth playback
- [ ] No audio glitches
- [ ] Transition smoothness
- [ ] Subtitle readability

## Quality Thresholds

| Metric | Minimum | Target |
|--------|---------|--------|
| Resolution | 1080p | 1080p+ |
| Audio Peak | -3dB | -2dB |
| Bitrate | 5Mbps | 10Mbps+ |
| Subtitle Sync | ±0.5s | ±0.2s |

## Workflow

### 1. Technical Verification
Check all technical specs.

### 2. Content Review
Verify content accuracy.

### 3. Playback Test
Test on target devices.

### 4. Platform Check
Verify platform requirements.

### 5. Final Approval
Issue delivery or revision.

## Input Contract

```yaml
final_video_path: string
target_platform: string
requirements: object
```

## Output Contract

```yaml
quality_report:
  overall_status: "approved"  # approved, needs_revision, rejected
  
  technical_qc:
    resolution:
      actual: "1080x1920"
      target: "1080x1920"
      status: "pass"
      
    frame_rate:
      actual: 30
      target: 30
      status: "pass"
      
    bitrate:
      actual: "12Mbps"
      target: "10Mbps+"
      status: "pass"
      
    audio:
      sync: "perfect"
      peak_level: "-2.1dB"
      quality: "excellent"
      status: "pass"
      
    visual_quality:
      artifacts: "none"
      color_accuracy: "good"
      sharpness: "good"
      status: "pass"
      
  content_qc:
    script_accuracy:
      script_followed: true
      missing_content: []
      extra_content: []
      status: "pass"
      
    subtitle_check:
      timing_accuracy: "good"
      readability: "excellent"
      spelling_errors: 0
      status: "pass"
      
    visual_relevance:
      content_match: "high"
      style_consistency: "high"
      status: "pass"
      
  platform_compliance:
    platform: "douyin"
    duration:
      actual: 42.5
      limit: 300
      status: "pass"
    aspect_ratio:
      actual: "9:16"
      target: "9:16"
      status: "pass"
    file_size:
      actual: "45MB"
      limit: "500MB"
      status: "pass"
    format:
      actual: "MP4/H.264"
      supported: true
      status: "pass"
      
  issues_found:
    blocking: []
    minor:
      - "Very slight audio ducking at 12s could be smoother"
      
  recommendations:
    - "Consider slight music volume increase in final 5 seconds"
    
  delivery_ready: true
  
  final_artifacts:
    - path: "work/videos/task/final-1.mp4"
      type: "primary"
      status: "ready"
    - path: "work/videos/task/subtitle.srt"
      type: "subtitle"
      status: "ready"