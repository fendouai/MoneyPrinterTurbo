---
name: video-footage-scout
description: Search and discover video footage from multiple stock sources. Matches visual requirements to available footage with precision.
---

# Video Footage Scout

## Core Job

Use this skill to **search and discover the best footage** from available stock sources.

This layer owns:

- keyword optimization
- multi-source searching
- footage discovery
- candidate collection
- initial filtering

## Stock Sources

### Primary Sources
| Source | Strengths | Best For |
|--------|-----------|----------|
| Pexels | Large library, diverse | General use |
| Pixabay | Curated quality | Professional scenes |
| Coverr | Themed collections | Specific moods |
| Mixkit | Creative shots | Artistic content |

### Source Selection Strategy
1. Start with Pexels (largest library)
2. Cross-reference with Pixabay
3. Use specialty sources for unique needs

## Search Strategy

### 1. Keyword Development

From visual requirements, develop search terms:

```
Visual need: "Busy professional in modern office"
↓
Search terms:
- Primary: "busy office worker"
- Variations: "professional working", "office multitasking"
- Context: "corporate office", "modern workspace"
- Emotion: "stressed professional", "focused worker"
```

### 2. Search Execution

For each scene:
- Search primary terms
- Try variations
- Check related terms
- Note source URLs

### 3. Initial Filtering

Quick assessment:
- Relevance to script
- Quality level
- Aspect ratio potential
- Licensing suitability

## Workflow

### 1. Process Visual Plan
Extract search requirements from each scene.

### 2. Develop Search Terms
Create optimized search terms for each scene.

### 3. Execute Multi-Source Search
Search across sources systematically.

### 4. Collect Candidates
Gather URLs and metadata for candidates.

### 5. Initial Filter
Remove obviously unsuitable options.

## Input Contract

```yaml
visual_plan: object
mood_direction: object
duration_requirement: int
aspect_ratio: string
```

## Output Contract

```yaml
footage_candidates:
  scene_1:
    visual_requirement: "Busy professional"
    search_terms_used:
      - "busy office worker"
      - "professional multitasking"
      - "corporate stress"
    candidates:
      - source: "pexels"
        url: "https://www.pexels.com/video/..."
        id: "12345"
        duration: 15
        resolution: "1920x1080"
        preview_url: "https://..."
        relevance_score: 9
        mood_match: "high"
        notes: "Perfect match for busy professional scene"
        
      - source: "pexels"
        url: "https://www.pexels.com/video/..."
        id: "12346"
        duration: 20
        resolution: "1920x1080"
        preview_url: "https://..."
        relevance_score: 7
        mood_match: "medium"
        notes: "Good alternative, slightly less dynamic"
        
  scene_2:
    visual_requirement: "Overwhelmed feeling"
    search_terms_used:
      - "stressed worker"
      - "overwhelmed office"
      - "tired professional"
    candidates:
      - source: "pixabay"
        url: "https://pixabay.com/videos/..."
        id: "67890"
        duration: 12
        resolution: "1920x1080"
        preview_url: "https://..."
        relevance_score: 8
        mood_match: "high"
        notes: "Good emotional match"
        
  search_summary:
    total_candidates: 24
    sources_used: ["pexels", "pixabay"]
    coverage_assessment: "Good coverage for all scenes"
    gaps_identified:
      - scene: "insight moment"
        note: "Could use more 'clarity' focused footage"
        
  recommendations:
    "Consider re-searching with 'meditation office' for insight scene"
    "Check vertical versions of selected clips"