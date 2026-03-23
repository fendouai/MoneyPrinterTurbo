---
name: video-voice-casting
description: Select the optimal voice for the video content. Matches voice characteristics to content type, audience, and emotional tone.
---

# Video Voice Casting

## Core Job

Use this skill to **select the perfect voice** that matches the content and audience.

This layer owns:

- voice analysis
- voice matching
- voice selection
- A/B voice comparison
- voice-direction alignment

## Voice Selection Factors

### 1. Language & Accent
- Native accent preferred
- Regional considerations
- Pronunciation clarity

### 2. Gender Consideration
- Content type appropriateness
- Audience preference
- Brand voice consistency

### 3. Age & Tone
- Youthful (18-25): Energetic, relatable
- Adult (25-45): Professional, trustworthy
- Mature (45+): Authoritative, wise

### 4. Emotional Range
- Warm & Friendly
- Professional & Authoritative
- Energetic & Upbeat
- Calm & Soothing
- Dramatic & Intense

## Voice Database

### Chinese (zh-CN)
| Voice | Gender | Tone | Best For |
|-------|--------|------|----------|
| XiaoxiaoNeural | Female | Warm, friendly | Lifestyle, education |
| YunxiNeural | Male | Youthful, energetic | Tech, entertainment |
| XiaoyiNeural | Female | Sweet, gentle | Emotional, storytelling |
| YunjianNeural | Male | Professional | Business, documentary |

### English (en-US)
| Voice | Gender | Tone | Best For |
|-------|--------|------|----------|
| JennyNeural | Female | Friendly, warm | General use |
| GuyNeural | Male | Professional | Business |
| AriaNeural | Female | Expressive | Storytelling |
| DavisNeural | Male | Deep, authoritative | Documentary |

## Workflow

### 1. Analyze Content Requirements
- Content type
- Target audience
- Emotional tone
- Platform culture

### 2. Match Voice Characteristics
- Gender preference
- Age range
- Tone style
- Pace suitability

### 3. Select Candidates
- Primary voice
- Alternative voices
- Backup options

### 4. Test & Validate
- Sample synthesis
- Tone check
- Audience fit

## Input Contract

```yaml
script: object
topic_analysis: object
mood_direction: object
voice_preferences:
  gender: string        # optional
  tone: string          # optional
  language: string
```

## Output Contract

```yaml
voice_casting:
  content_analysis:
    content_type: "educational"
    emotional_tone: "inspiring, warm"
    pace_requirement: "moderate"
    audience: "working professionals 25-35"
    
  voice_requirements:
    language: "zh-CN"
    gender_preference: "female"
    tone_style: "warm, professional, friendly"
    age_range: "adult"
    emotional_range: "can convey inspiration and encouragement"
    
  voice_candidates:
    - name: "zh-CN-XiaoxiaoNeural"
      gender: "female"
      description: "Warm, friendly, professional"
      pros: ["Natural warmth", "Clear articulation", "Versatile"]
      cons: ["May feel too casual for very serious content"]
      suitability_score: 9
      sample_text: "你有没有发现，越是忙碌的人，反而越有时间？"
      
    - name: "zh-CN-XiaoyiNeural"
      gender: "female"
      description: "Sweet, gentle, soothing"
      pros: ["Very pleasant", "Good for emotional content"]
      cons: ["May lack authority for business content"]
      suitability_score: 7
      
  selected_voice:
    primary:
      name: "zh-CN-XiaoxiaoNeural"
      full_name: "zh-CN-XiaoxiaoNeural-Female"
      rationale: "Perfect balance of warmth and professionalism for educational content"
      
    backup:
      name: "zh-CN-YunxiNeural"
      full_name: "zh-CN-YunxiNeural-Male"
      rationale: "Good alternative if male voice preferred"
      
  delivery_guidance:
    overall_pace: "moderate"
    emphasis_words: ["反而", "真相是", "最重要"]
    pause_suggestions:
      - position: "after hook"
        duration: "0.3s"
    tone_variation:
      hook: "curious, engaging"
      body: "warm, informative"
      landing: "encouraging, confident"