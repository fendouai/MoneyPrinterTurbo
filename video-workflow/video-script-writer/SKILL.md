---
name: video-script-writer
description: Write the video script following the architectural blueprint. Focuses on conversational tone, mobile-first readability, and emotional resonance.
---

# Video Script Writer

## Core Job

Use this skill to **write the actual script content** following the structure and research.

This layer owns:

- script writing
- tone calibration
- language adaptation
- mobile readability
- conversational flow

## Writing Principles

### Mobile-First Writing

- Short sentences (avg 15-20 chars in Chinese)
- One idea per sentence
- No complex clauses
- Speak, don't write
- Rhythm and flow over grammar

### Emotional Resonance

- Show, don't tell
- Use sensory language
- Include specific details
- Create mental images
- Make it personal

### Value Delivery

- Front-load the value
- Make every word earn its place
- No filler content
- Pay off the promise
- Exceed expectations

## Workflow

### 1. Hook Delivery (0-3s)
Execute the selected hook with:
- Confident tone
- Clear articulation
- Immediate engagement

### 2. Body Content
Write following architecture:
- Follow section structure
- Maintain pacing
- Deliver on hook promise
- Build to climax

### 3. Landing/CTA
Strong finish with:
- Clear takeaway
- Emotional payoff
- Natural CTA

### 4. Polish
Review and refine:
- Read aloud test
- Timing check
- Clarity check
- Remove redundancy

## Input Contract

```yaml
topic_analysis: object
research_brief: object
architecture: object
selected_hook: object
language: string
```

## Output Contract

```yaml
script:
  full_text:
  word_count:
  estimated_duration:
  
  sections:
    - name: "hook"
      text: "你有没有发现，越是忙碌的人，反而越有时间？"
      duration: 2.5
      
    - name: "problem_setup"
      text: "每天都在忙，但回头一看，好像什么都没做成。"
      duration: 4
      
    - name: "insight"
      text: "真相是，时间从来不是问题。问题是你把注意力都花在了哪儿。"
      duration: 6
      
    - name: "solution"
      text: "真正高效的人，不是时间多，而是懂得把最重要的事，放在精力最好的时候做。"
      duration: 8
      
    - name: "landing"
      text: "记住，忙碌不等于高效。学会取舍，才能做到极致。"
      duration: 4

  tone_notes:
    overall: "conversational, warm, slightly provocative"
    hook: "curious, relatable"
    body: "insightful, grounded"
    landing: "encouraging, memorable"

  delivery_guide:
    pace: "moderate, slightly faster on hook"
    emphasis_words: ["反而", "真相是", "最重要"]
    pauses: ["after '反而越有时间'", "before '真相是'"]
    
  golden_lines:
    - "时间从来不是问题。问题是你把注意力都花在了哪儿。"
    - "忙碌不等于高效。学会取舍，才能做到极致。"
```

## Quality Checklist

- [ ] Hook delivers in under 3 seconds
- [ ] Every sentence has purpose
- [ ] Read aloud sounds natural
- [ ] No jargon without explanation
- [ ] Ending is memorable
- [ ] Estimated timing matches target
- [ ] At least 1 quotable line (golden line)