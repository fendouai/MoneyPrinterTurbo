---
name: video-hook-craftsman
description: Design and craft powerful opening hooks that stop the scroll. Specializes in first-3-second attention capture, pattern interrupts, and curiosity triggers.
---

# Video Hook Craftsman

## Core Job

Use this skill to **create the critical first 3 seconds** that determine whether viewers stay or scroll.

This layer owns:

- opening hook design
- pattern interrupts
- curiosity triggers
- first-frame decisions
- scroll-stopping techniques

## Hook Types

### 1. Question Hook
Pose a provocative question that demands mental engagement.

```
"你有没有发现，越是忙碌的人，反而越有时间？"
"为什么90%的时间管理方法都失败了？"
```

### 2. Statement Hook
Make a bold, surprising claim.

```
"时间管理的最大谎言：你需要更多时间。"
"我花了10年才明白这件事..."
```

### 3. Story Hook
Start mid-story with tension.

```
"那是凌晨3点，我终于明白了..."
"当我看到这个数据时，我惊呆了..."
```

### 4. Contrarian Hook
Challenge common belief.

```
"大家都在做时间管理，但方向完全错了。"
"番茄工作法？那是给新手用的。"
```

### 5. Number Hook
Use specific numbers for credibility.

```
"每天只需要17分钟，就能..."
"这个方法帮我节省了3小时..."
```

### 6. Pain Point Hook
Directly address audience pain.

```
"又加班到深夜，但事情还是没做完？"
"明明忙了一整天，却感觉什么都没完成？"
```

### 7. Curiosity Gap Hook
Create information gap.

```
"这个秘密，只有1%的人知道..."
"我发现了一个惊人的规律..."
```

## Workflow

### 1. Analyze Audience State
What are they doing when they see this?
- Scrolling mindlessly
- Looking for entertainment
- Seeking solutions
- Killing time

### 2. Select Hook Strategy
Match hook type to:
- Content type
- Platform culture
- Emotional tone
- Audience mindset

### 3. Craft Multiple Versions
Create 5+ hook variations:
- Different hook types
- Different emotional angles
- Different lengths (1-3 seconds)

### 4. Test Criteria
Evaluate hooks on:
- Pattern interrupt strength (1-10)
- Curiosity gap (1-10)
- Emotional resonance (1-10)
- Brand alignment (1-10)

## Input Contract

```yaml
topic_analysis: object
architecture: object
hook_requirements: object
```

## Output Contract

```yaml
hook_candidates:
  - type: "question"
    content: "你有没有发现，越是忙碌的人，反而越有时间？"
    duration: 2.5
    scores:
      pattern_interrupt: 8
      curiosity_gap: 9
      emotional_resonance: 8
      brand_alignment: 9
    rationale: "直接击中痛点，制造认知冲突"
    
  - type: "contrarian"
    content: "时间管理的最大谎言：你需要更多时间。"
    duration: 3
    scores:
      pattern_interrupt: 9
      curiosity_gap: 9
      emotional_resonance: 7
      brand_alignment: 8
    rationale: "颠覆认知，强好奇心驱动"

selected_hook:
  type:
  content:
  duration:
  first_frame_visual:  # 建议的视觉配合
  delivery_note:       # 语调建议

hook_variations:
  platform_optimized:
    douyin: "你有没有发现..."
    bilibili: "今天想和大家聊聊一个反直觉的现象..."
    video_account: "很多人问我，怎么才能更高效..."
```

## Hook Formula

```
Hook Power = (Pattern Interrupt × Curiosity) / Time to Payoff
```

- Higher pattern interrupt = stops the scroll
- Higher curiosity = creates anticipation
- Lower time to payoff = faster reward for staying