---
name: video-seo-specialist
description: Optimize video discoverability through SEO, hashtags, descriptions, and metadata optimization.
---

# Video SEO Specialist

## Core Job

Use this skill to **maximize video discoverability** through SEO optimization.

This layer owns:

- keyword research
- hashtag strategy
- description optimization
- metadata
- search ranking

## SEO Best Practices

### 1. Title Optimization
- Front-load important keywords
- Include numbers when relevant
- Create curiosity without clickbait

### 2. Description Optimization
- First 2 lines show without expansion
- Include relevant keywords naturally
- Add timestamps for longer content

### 3. Hashtag Strategy
- 3-5 highly relevant hashtags
- Mix broad and niche tags
- Platform-specific usage

## Input Contract

```yaml
video_topic: string
content_analysis: object
target_platform: string
```

## Output Contract

```yaml
seo_optimization:
  title:
    primary: "为什么你总是时间不够用？"
    alternatives:
      - "时间管理的最大谎言"
      - "高效人士不会告诉你的时间秘密"
      
  description:
    full: |
      你有没有发现，越是忙碌的人，反而越有时间？
      
      在这个视频里，我会告诉你：
      • 时间管理的真正秘密
      • 为什么你总是觉得时间不够
      • 3个立刻提升效率的方法
      
      收藏起来，慢慢看。
      
    first_2_lines: "你有没有发现，越是忙碌的人，反而越有时间？..."
    
  hashtags:
    primary:
      - "#时间管理"
      - "#效率"
      - "#职场干货"
    secondary:
      - "#自我提升"
      - "#成长思维"
      - "#工作效率"
    total_count: 5
    
  metadata:
    category: "Education"
    tags:
      - "time management"
      - "productivity"
      - "work efficiency"
      - "self improvement"
    language: "zh-CN"