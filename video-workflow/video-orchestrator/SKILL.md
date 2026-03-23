---
name: video-orchestrator
description: Use this skill as the top-level workflow for turning a video topic into a complete short video. It coordinates all layers from topic analysis to final video export, following a precise pipeline order. Use when the user gives a topic and wants the full professional pipeline run instead of handling each step manually.
---

# Video Orchestrator

Use this as the **entry skill** for the complete professional video production workflow.

This skill does **not** replace specialized skills. It decides **order, required outputs, and handoff rules** between them.

## Complete Pipeline (21 Steps)

### Phase 1: Content & Script (7 steps)

1. `video-topic-analyzer` - Strategic topic analysis
2. `video-content-researcher` - Deep content research
3. `video-script-architect` - Script structure design
4. `video-hook-craftsman` - Hook creation
5. `video-script-writer` - Script writing
6. `video-script-reviewer` - Script quality review
7. `video-cta-strategist` - Call-to-action design

### Phase 2: Visual (5 steps)

8. `video-visual-planner` - Visual requirements planning
9. `video-mood-director` - Mood and atmosphere direction
10. `video-footage-scout` - Footage discovery
11. `video-footage-curator` - Footage selection
12. `video-visual-validator` - Visual validation

### Phase 3: Audio (4 steps)

13. `video-voice-casting` - Voice talent selection
14. `video-speech-director` - Speech direction
15. `video-sound-designer` - Music and sound design
16. `video-audio-engineer` - Audio production

### Phase 4: Post-Production (5 steps)

17. `video-timing-editor` - Timing and pacing
18. `video-subtitle-stylist` - Subtitle styling
19. `video-transition-artist` - Transition design
20. `video-colorist` - Color grading
21. `video-quality-controller` - Final QC

### Phase 5: Optimization (3 steps - optional)

22. `video-platform-optimizer` - Platform optimization
23. `video-thumbnail-designer` - Thumbnail design
24. `video-seo-specialist` - SEO optimization

## Operating Rules

1. **Never skip phases** - Execute in order
2. **Each layer passes only what the next layer needs**
3. **Block if any layer fails** - Fix before proceeding
4. **Always run quality control** before delivery
5. **Optimize for platform** before publishing

## Handoff Contract

### Content Phase
```
topic-analyzer → content-researcher: topic_analysis
content-researcher → script-architect: research_brief
script-architect → hook-craftsman: architecture
hook-craftsman → script-writer: selected_hook
script-writer → script-reviewer: script draft
script-reviewer → cta-strategist: approved_script
cta-strategist → visual-planner: final_script + cta
```

### Visual Phase
```
visual-planner → mood-director: visual_plan
mood-director → footage-scout: mood_direction
footage-scout → footage-curator: footage_candidates
footage-curator → visual-validator: curated_selection
visual-validator → voice-casting: validated_materials
```

### Audio Phase
```
voice-casting → speech-director: selected_voice
speech-director → sound-designer: speech_direction
sound-designer → audio-engineer: sound_design
audio-engineer → timing-editor: final_audio
```

### Post-Production Phase
```
timing-editor → subtitle-stylist: timing_plan
subtitle-stylist → transition-artist: subtitle_style
transition-artist → colorist: transition_design
colorist → quality-controller: color_graded_video
quality-controller → platform-optimizer: approved_video
```

## Final Deliverables

After full pipeline:

```
work/videos/{task_id}/
├── script.json              # Final script with metadata
├── terms.json               # Search terms
├── audio.mp3               # Final audio mix
├── subtitle.srt             # Subtitles
├── materials/               # Downloaded video clips
├── combined.mp4            # Combined video (no subs)
├── final.mp4               # Final video
├── thumbnail.png            # Thumbnail
├── metadata.json            # SEO and platform metadata
└── quality-report.json      # QC report
```

## Parallel Execution

Some phases **CAN** run in parallel:

- Phase 1 steps 2-7: After topic analysis, script work is independent
- Phase 2 steps 10-11: Footage scouting and curating can overlap
- Phase 3 steps 13-15: Voice casting and sound design can start after script is done

Most phases **MUST** be sequential:

- Phase 1 must complete before Phase 2 starts
- Phase 2 must complete before Phase 3 starts
- Phase 3 must complete before Phase 4 starts
- Phase 4 must complete before Phase 5 starts

## Error Recovery

If any step fails:

1. Log the failure with full context
2. Save all partial outputs
3. Identify root cause
4. Fix and retry from failed step
5. Never skip steps to "catch up"

## Minimal Run (Quick Mode)

For rapid testing, use only essential steps:

1. `video-topic-analyzer`
2. `video-script-writer`
3. `video-voice-casting`
4. `video-audio-engineer`
5. `video-footage-curator`
6. `video-timing-editor`
7. `video-quality-controller`

This produces a basic video in ~7 steps vs full 21-step pipeline.