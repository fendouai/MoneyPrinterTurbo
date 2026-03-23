---
name: video-topic-analyzer
description: Analyze video topic before content creation. Identifies target audience, content type, emotional tone, and platform suitability. Use this skill first to establish the creative direction for the entire video production pipeline.
---

# Video Topic Analyzer

## Core Job

Use this skill to **analyze and define the strategic direction** before any content creation begins.

This layer owns:

- topic decomposition
- audience identification
- platform analysis
- content type selection
- emotional tone setting
- competitive landscape scan

## Workflow

### 1. Decompose the Topic

Ask:

- What is the core subject?
- What are the key sub-themes?
- What angle hasn't been explored?
- What makes this topic timely?

### 2. Identify Target Audience

Define:

- Primary audience demographic
- Secondary audience segments
- Audience pain points
- Audience aspirations
- Where they consume content

### 3. Select Content Type

Choose one primary type:

| Type | Structure | Best For |
|------|-----------|----------|
| educational | concept → explanation → example → takeaway | Teaching, tutorials |
| motivational | problem → insight → action → transformation | Self-improvement |
| storytelling | context → challenge → resolution → lesson | Case studies, history |
| entertainment | hook → twist → payoff | Viral content |
| persuasive | problem → solution → proof → CTA | Product/service |

### 4. Determine Emotional Tone

Select primary emotion:

- Inspiring / Uplifting
- Educational / Informative
- Controversial / Thought-provoking
- Emotional / Heartwarming
- Humorous / Lighthearted
- Dramatic / Intense

### 5. Analyze Platform Fit

| Platform | Duration | Format | Audience |
|----------|----------|--------|----------|
| Douyin/TikTok | 15-60s | Fast-paced, hook-driven | Gen Z, millennials |
| YouTube Shorts | 30-60s | Story-driven, value-focused | Broad |
| Instagram Reels | 15-90s | Visual, aesthetic | 18-34 |
| Bilibili | 1-5min | Deep, detailed | 16-35, tech-savvy |
| Video Account | 30s-3min | Practical, relatable | 25-45, professionals |

## Input Contract

```yaml
video_topic: string
platform: string        # Optional
target_audience: string # Optional
content_goal: string    # Optional
```

## Output Contract

```yaml
topic_analysis:
  core_subject:
  sub_themes:
  unique_angle:

audience:
  primary:
  secondary:
  pain_points:
  aspirations:

content_strategy:
  content_type:
  emotional_tone:
  duration_target:
  platform_primary:
  platform_secondary:

competitive_landscape:
  common_angles:
  gap_opportunity:
  differentiation:

creative_brief:
  headline:
  key_message:
  emotional_goal:
  success_metrics:
```

## Example

Input:
```yaml
video_topic: "时间管理"
platform: "douyin"
```

Output:
```yaml
topic_analysis:
  core_subject: "时间管理方法"
  sub_themes: ["效率提升", "优先级决策", "精力管理"]
  unique_angle: "不是管理时间，而是管理注意力和精力"

audience:
  primary: "25-35岁职场人，工作忙碌但效率不高"
  secondary: "学生群体，需要平衡学习与生活"
  pain_points: ["总是感觉时间不够用", "忙碌但产出低", "容易分心"]
  aspirations: ["高效完成工作", "拥有更多自由时间", "减少焦虑感"]

content_strategy:
  content_type: "educational"
  emotional_tone: "inspiring"
  duration_target: "45s"
  platform_primary: "douyin"
  platform_secondary: "video_account"

competitive_landscape:
  common_angles: ["时间管理工具推荐", "早起的好处", "番茄工作法"]
  gap_opportunity: "很少有人讲注意力和精力的管理，而不仅仅是时间"
  differentiation: "从认知层面切入，而非工具层面"

creative_brief:
  headline: "为什么你总是时间不够用"
  key_message: "真正的时间管理是注意力和精力管理"
  emotional_goal: "让观众意识到问题根源，产生改变的动力"
  success_metrics: ["完播率>60%", "评论互动>100", "收藏>200"]
```