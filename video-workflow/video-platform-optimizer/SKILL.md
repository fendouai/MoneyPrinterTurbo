---
name: video-platform-optimizer
description: Optimize video for specific platform requirements, specs, and audience behavior patterns.
---

# Video Platform Optimizer

## Core Job

Use this skill to **optimize the video** for specific platform requirements and best practices.

This layer owns:

- platform requirements
- spec optimization
- algorithm factors
- hashtag strategy
- posting strategy

## Platform Specifications

| Platform | Duration | Aspect | Resolution | Max Size |
|----------|----------|--------|------------|----------|
| Douyin | 15s-5min | 9:16 | 1080x1920 | 500MB |
| TikTok | 15s-10min | 9:16 | 1080x1920 | 500MB |
| YouTube Shorts | 15-60s | 9:16 | 1080x1920 | 500MB |
| Instagram Reels | 15-90s | 9:16 | 1080x1920 | 100MB |
| Bilibili | 1min+ | 16:9 | 1920x1080 | 2GB |

## Optimization Factors

### 1. Duration Optimization
- Douyin: 30-45s optimal for retention
- YouTube Shorts: 30-45s optimal
- TikTok: 21-34s for viral potential

### 2. Algorithm Factors
- First 3 seconds critical
- Engagement signals matter
- Watch time optimization
- Caption/subtitle boost

### 3. Format Optimization
- Correct aspect ratio
- Safe zones for text
- Thumbnail considerations

## Input Contract

```yaml
final_video_path: string
target_platforms: list
content_analysis: object
```

## Output Contract

```yaml
platform_optimization:
  douyin:
    status: "optimized"
    recommended_duration: "35-45s"
    hashtags:
      - "#时间管理"
      - "#职场干货"
      - "#效率神器"
      - "#成长"
    posting_time: "12:00-13:00, 20:00-22:00"
    caption_template: "你有没有发现...\n\n#话题1 #话题2 #话题3\n\n关注我，获取更多干货"
    algorithm_tips:
      - "Hook in first 2 seconds"
      - "Encourage comments with question"
      - "Prompt saves with '收藏起来'"
      
  youtube_shorts:
    status: "optimized"
    recommended_duration: "30-45s"
    hashtags:
      - "#timemanagement"
      - "#productivity"
      - "#lifehacks"
    posting_time: "14:00-16:00, 19:00-21:00"
    
  bilibili:
    status: "optimized"
    recommended_duration: "1-3min"
    hashtags:
      - "#效率提升"
      - "#时间管理"
      - "#职场进化论"
    posting_time: "18:00-22:00"