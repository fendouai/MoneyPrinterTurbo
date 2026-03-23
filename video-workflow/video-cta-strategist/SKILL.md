---
name: video-cta-strategist
description: Design effective calls-to-action that drive engagement, conversion, or brand objectives. Matches CTA to content type and audience psychology.
---

# Video CTA Strategist

## Core Job

Use this skill to **design the closing call-to-action** that drives desired audience behavior.

This layer owns:

- CTA strategy selection
- CTA wording
- Placement optimization
- Engagement driver design

## CTA Types

### 1. Engagement CTAs
Drive platform engagement.

```
"你觉得呢？评论区聊聊"
"认同的点个赞"
"收藏起来，慢慢看"
"关注我，持续更新"
```

### 2. Conversion CTAs
Drive specific actions.

```
"点击链接，立即体验"
"回复'时间管理'，获取完整方法"
"私信我，一对一解答"
```

### 3. Content CTAs
Drive content consumption.

```
"下期告诉你具体怎么做"
"主页有更多干货"
"这个系列的下一篇更精彩"
```

### 4. Brand CTAs
Build brand association.

```
"我是XX，陪你一起成长"
"记得关注，我们下期见"
```

### 5. Implicit CTAs
No explicit ask, but drives behavior.

```
"你也可以试试这个方法"
"希望对你有帮助"
```

## CTA Strategy Selection

| Content Type | Primary CTA | Secondary CTA |
|--------------|-------------|---------------|
| Educational | Save + Follow | Comment |
| Motivational | Like + Follow | Share |
| Entertainment | Like + Share | Follow |
| Promotional | Click Link | Comment |

## Workflow

### 1. Identify Goal
What behavior do we want?
- Engagement (like, comment, share, save)
- Conversion (click, purchase, signup)
- Retention (follow, subscribe)
- Brand (remember, trust)

### 2. Match to Content
CTA should feel natural:
- Educational content → save/follow
- Emotional content → share/comment
- Promotional content → click/purchase

### 3. Craft Wording
Effective CTA language:
- Direct and clear
- Low friction
- Immediate benefit
- Personal where possible

### 4. Optimize Placement
Timing matters:
- Natural endpoint
- After emotional payoff
- Before attention drops

## Input Contract

```yaml
script: object
topic_analysis: object
cta_goal: string        # engagement/conversion/retention/brand
```

## Output Contract

```yaml
cta_strategy:
  primary_goal:
  secondary_goal:
  
  cta_options:
    - type: "engagement"
      action: "comment"
      wording: "你有什么时间管理的小技巧？评论区分享一下"
      placement: "end"
      psychology: "Invites sharing, creates community"
      
    - type: "retention"
      action: "follow"
      wording: "关注我，下期告诉你具体怎么做"
      placement: "end"
      psychology: "Creates anticipation, builds relationship"

  selected_cta:
    primary:
      type:
      wording:
      placement:
    secondary:
      type:
      wording:
      placement:
      
  integration:
    script_placement: "After '学会取舍，才能做到极致'"
    transition: "自然过渡到互动"
    timing: "最后3秒"
    
  a_b_suggestions:
    - version_a: "评论区聊聊你的看法"
      version_b: "你觉得呢？评论区见"
      recommendation: "Version B is more conversational"
```