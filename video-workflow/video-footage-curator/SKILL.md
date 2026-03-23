---
name: video-footage-curator
description: Curate and select the best footage from candidates. Evaluates quality, relevance, mood match, and technical suitability.
---

# Video Footage Curator

## Core Job

Use this skill to **select the best footage** from discovered candidates.

This layer owns:

- footage evaluation
- quality assessment
- mood matching
- selection decision
- sequence planning

## Evaluation Criteria

### 1. Relevance (30%)
How well does it match the script?
- Subject match
- Action match
- Context match
- Story support

### 2. Quality (25%)
Technical quality of footage:
- Resolution
- Lighting quality
- Stability
- Color quality

### 3. Mood Match (25%)
Does it fit the emotional direction?
- Tone alignment
- Color consistency
- Style coherence
- Emotional resonance

### 4. Usability (20%)
Can it be used effectively?
- Duration sufficiency
- Edit flexibility
- Aspect ratio potential
- Transition compatibility

## Selection Process

### 1. Score Each Candidate

```
Candidate A:
- Relevance: 9/10 - Perfect subject match
- Quality: 8/10 - High res, good lighting
- Mood: 9/10 - Matches inspirational tone
- Usability: 8/10 - Good duration, flexible
- Total: 8.5/10
```

### 2. Compare Within Scenes
Select best 2-3 options per scene.

### 3. Check Sequence Flow
Ensure selected clips work together:
- Visual continuity
- Color consistency
- Mood progression

### 4. Final Selection
Choose primary and backup clips.

## Input Contract

```yaml
footage_candidates: object
mood_direction: object
visual_plan: object
```

## Output Contract

```yaml
curated_selection:
  scene_1:
    selected:
      - source: "pexels"
        id: "12345"
        url: "https://www.pexels.com/video/..."
        duration: 15
        start_point: 0
        end_point: 5
        scores:
          relevance: 9
          quality: 8
          mood: 9
          usability: 8
          total: 8.5
        selection_rationale: "Perfect busy professional shot, great energy"
        
    backup:
      - source: "pexels"
        id: "12346"
        rationale: "Good alternative if primary doesn't crop well"
        
  scene_2:
    selected:
      - source: "pixabay"
        id: "67890"
        url: "https://pixabay.com/videos/..."
        duration: 12
        start_point: 2
        end_point: 7
        scores:
          relevance: 8
          quality: 9
          mood: 8
          usability: 9
          total: 8.25
        selection_rationale: "Excellent quality, good emotional match"

  sequence_review:
    flow_assessment: "Good progression from busy to calm"
    color_consistency: "All clips have warm, natural tones"
    mood_progression: "Follows script emotional arc well"
    total_duration: 48
    duration_variance: "+3s from audio duration"
    
  edit_notes:
    - clip: "scene_1_selected"
      note: "May need slight color adjustment to match scene 2"
    - clip: "scene_3_selected"
      note: "Consider slow-motion effect for emphasis"
      
  download_queue:
    - scene: 1
      source: "pexels"
      id: "12345"
      priority: "high"
    - scene: 2
      source: "pixabay"
      id: "67890"
      priority: "high"