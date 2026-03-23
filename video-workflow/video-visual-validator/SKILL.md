---
name: video-visual-validator
description: Validate that selected footage meets all requirements before download. Checks technical specs, licensing, and content appropriateness.
---

# Video Visual Validator

## Core Job

Use this skill to **validate footage selections** before committing to download and use.

This layer owns:

- technical validation
- license verification
- content appropriateness
- requirement matching
- final approval

## Validation Checklist

### 1. Technical Requirements
- [ ] Resolution meets minimum (1080p for vertical)
- [ ] Frame rate acceptable (24/25/30 fps)
- [ ] Codec compatible (H.264 preferred)
- [ ] No visible artifacts or compression issues
- [ ] Stable footage (or intentional movement)

### 2. Content Requirements
- [ ] Subject matches script context
- [ ] No brand names or logos visible
- [ ] No recognizable faces (if needed)
- [ ] Appropriate for target audience
- [ ] No controversial elements

### 3. License Requirements
- [ ] Commercial use allowed
- [ ] Attribution requirements noted
- [ ] Modification allowed
- [ ] No model release issues (if applicable)

### 4. Edit Requirements
- [ ] Duration sufficient for planned use
- [ ] Edit points available
- [ ] Works in target aspect ratio
- [ ] Color grading potential

## Validation Process

### 1. Technical Check
Verify specs and quality.

### 2. Content Review
Watch for any issues.

### 3. License Verification
Confirm usage rights.

### 4. Edit Feasibility
Confirm can be used as planned.

### 5. Final Decision
Approve or flag for replacement.

## Input Contract

```yaml
curated_selection: object
requirements:
  min_resolution: string
  aspect_ratio: string
  license_type: string
  content_guidelines: list
```

## Output Contract

```yaml
validation_results:
  scene_1:
    clip_id: "12345"
    status: "approved"
    
    technical_check:
      resolution: "1920x1080"
      frame_rate: 30
      codec: "H.264"
      quality_issues: []
      status: "pass"
      
    content_check:
      subject_match: true
      visible_brands: []
      visible_faces: "unrecognizable"
      audience_appropriate: true
      controversial_elements: []
      status: "pass"
      
    license_check:
      commercial_use: true
      attribution_required: false
      modification_allowed: true
      model_release: "not required"
      status: "pass"
      
    edit_check:
      duration_sufficient: true
      edit_points: "multiple clean cuts available"
      aspect_ratio_works: "crops well to 9:16"
      color_grading_potential: "good"
      status: "pass"
      
    overall_status: "approved"
    
  scene_2:
    clip_id: "67890"
    status: "flagged"
    
    technical_check:
      resolution: "1920x1080"
      frame_rate: 25
      codec: "H.264"
      quality_issues: []
      status: "pass"
      
    content_check:
      subject_match: true
      visible_brands: ["Nike logo on shirt - 2 seconds visible"]
      visible_faces: "unrecognizable"
      audience_appropriate: true
      controversial_elements: []
      status: "flagged"
      
    license_check:
      commercial_use: true
      attribution_required: false
      modification_allowed: true
      model_release: "not required"
      status: "pass"
      
    edit_check:
      duration_sufficient: true
      edit_points: "available"
      aspect_ratio_works: "yes"
      color_grading_potential: "good"
      status: "pass"
      
    overall_status: "flagged"
    issue: "Nike logo visible at 3-5 seconds"
    recommendation: "Either blur logo or select alternative clip"
    
  summary:
    total_clips: 8
    approved: 7
    flagged: 1
    rejected: 0
    
  action_items:
    - "Replace or blur Nike logo in scene 2"
    
  download_ready: false