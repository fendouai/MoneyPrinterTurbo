---
name: video-content-researcher
description: Deep research on video topic before script writing. Gathers facts, statistics, expert quotes, real examples, and supporting evidence. Ensures content credibility and depth.
---

# Video Content Researcher

## Core Job

Use this skill to **gather supporting evidence and deepen content credibility** before writing.

This layer owns:

- fact collection
- statistics gathering
- expert quotes
- real-world examples
- counter-arguments research
- source verification

## Workflow

### 1. Core Facts Research

Collect:

- Key definitions
- Historical context
- Current trends
- Scientific backing (if applicable)

### 2. Statistics & Data

Find:

- Recent statistics
- Comparative data
- Trend data
- Source citations

### 3. Expert Perspectives

Gather:

- Authoritative quotes
- Expert opinions
- Industry insights
- Academic findings

### 4. Real Examples

Find:

- Case studies
- Success stories
- Failure examples
- Relatable scenarios

### 5. Counter-arguments

Research:

- Common misconceptions
- Opposing views
- Limitations and caveats

## Input Contract

```yaml
topic_analysis: object    # From video-topic-analyzer
depth: string             # "quick" or "deep"
```

## Output Contract

```yaml
research_brief:
  core_facts:
    - fact_1
    - fact_2
    
  statistics:
    - stat: "XX%"
      source: "来源"
      year: 2024
      
  expert_quotes:
    - quote: "引言内容"
      expert: "专家名称"
      context: "背景"
      
  real_examples:
    - title: "案例标题"
      summary: "案例摘要"
      outcome: "结果"
      
  misconceptions:
    - misconception: "常见误解"
      reality: "实际情况"
      
  sources:
    - title: "来源标题"
      url: "链接"
      credibility: "high/medium/low"
```

## Research Priority

1. Academic papers and peer-reviewed studies
2. Government and official statistics
3. Industry reports from reputable firms
4. Expert-authored books and articles
5. Verified news sources
6. User-generated content (use with caution)

## Quality Checklist

- [ ] At least 3 credible sources
- [ ] Statistics are recent (within 2 years)
- [ ] Expert quotes have context
- [ ] Real examples are verifiable
- [ ] Sources are cited properly