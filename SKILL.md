---
name: trend-harvester
version: 1.0.0
description: Trend Harvester - Research any topic across Reddit, Hacker News, X, YouTube in minutes. Generate actionable trend reports with sources. Trigger on: 'trending', 'what's hot', 'trend research', 'market research', 'popular in'.
emoji: 🌊
tags: [trends, research, market-analysis, automation, productivity]
---

# Trend Harvester 🌊

Research any topic across multiple platforms in minutes. Generate actionable trend reports.

Inspired by last30days-skill (23K GitHub stars) which proved cross-platform trend research is a killer feature.

## The Problem

You need to understand what's trending in a topic, but:
- Each platform shows different signals
- Manual research takes hours
- You miss important discussions on platforms you don't check
- No way to synthesize insights across sources

## The Solution: Multi-Platform Harvest Pipeline

```
Input: "AI agent frameworks"
Output: Trend report with data from 5+ platforms
```

### Platform Coverage

| Platform | What You Get | How to Access |
|----------|-------------|---------------|
| Hacker News | Tech discussions, developer sentiment | hn.algolia.com API |
| Reddit | Community opinions, use cases | web_fetch reddit search |
| GitHub | Code trends, star velocity | GitHub API |
| YouTube | Tutorial demand, creator attention | web_fetch search |
| Product Hunt | New tools, launch momentum | web_fetch |

### Pipeline Stages

#### Stage 1: Keyword Expansion (30 seconds)

```
Input: "AI agent frameworks"

Expanded search terms:
- Primary: "AI agent framework", "agent framework"
- Related: "AI agent skills", "agent workflow", "agentic AI"
- Platforms: "AI agent framework reddit", "AI agent framework hn"
- Code: "agent-framework github"
```

#### Stage 2: Multi-Platform Search (2 minutes)

```
For each platform:
1. Search with primary + related terms
2. Collect top 5 results per platform
3. Extract: title, url, score/comments, date
4. Note sentiment (positive/negative/neutral)
```

#### Stage 3: Synthesis (1 minute)

```
Combine findings:
- Group by theme
- Identify consensus across platforms
- Note platform-specific insights
- Rank by combined signal strength
```

#### Stage 4: Report Generation (1 minute)

```
Output format:

# Trend Report: [Topic]
**Date:** YYYY-MM-DD
**Platforms:** X sources analyzed
**Confidence:** High/Medium/Low

## 🔥 Top Trend

[Most significant finding across platforms]

## Key Findings

### Finding 1: [Title]
- **Signal:** Strong (seen on X platforms)
- **Platforms:** HN (pts), Reddit (upvotes), GitHub (stars)
- **Summary:** [1-2 sentence summary]
- **Actionable insight:** [What to do about it]

### Finding 2: [Title]
...

## Platform-Specific Insights

### Hacker News
- [What developers are saying]

### Reddit
- [What users are experiencing]

### GitHub
- [What builders are creating]

## Trend Direction
📈 Rising / 📊 Stable / 📉 Declining

## Recommended Actions
1. [Specific action based on trends]
2. [Specific action based on trends]

## Sources
- [Source 1](url)
- [Source 2](url)
```

## Usage Examples

### Quick Trend Check
```
User: "What's trending in AI agents?"

Agent:
[Expanding keywords...]
[Searching 5 platforms...]
[Synthesizing...]

## AI Agents - Trend Report (2026-04-21)

🔥 Top Trend: Multi-agent orchestration frameworks (Superpowers 161K⭐)

Key Findings:
1. Superpowers framework dominates (161K stars, 3 months)
2. Cognitive debt prevention is emerging concern (+23.5% incidents)
3. Skill activation rate (40%) is a known problem
4. MCP integration becoming standard

Recommended: Build skills with activation optimization
```

### Deep Dive
```
User: "Deep trend research on AI code review tools"

Agent:
[This will take 5-10 minutes for comprehensive analysis]

Stage 1/4: Keyword expansion...
- "AI code review", "automated PR review", "AI code quality"
- "code review automation github", "AI PR review"

Stage 2/4: Multi-platform search...
- HN: 8 discussions found
- Reddit: 5 threads found
- GitHub: 12 repos found
- YouTube: 6 videos found

Stage 3/4: Synthesis...
- 3 major trends identified
- 2 emerging patterns

Stage 4/4: Report generation...

[Full report saved to memory/trends/ai-code-review-2026-04-21.md]
```

### Competitive Landscape
```
User: "What are the trending AI agent skill frameworks?"

Agent:
[Generating competitive landscape...]

| Framework | Stars | Trend | Focus |
|-----------|-------|-------|-------|
| Superpowers | 161K | 📈 Rising | Mandatory workflows |
| agent-skills | 18K | 📈 Rising | Engineering lifecycle |
| xiaobai-skills | 0 | 🆕 New | AI reliability |

[Full landscape saved to memory/trends/skill-frameworks-2026-04-21.md]
```

## Trigger Phrases

This skill activates when:
- "what's trending in..."
- "trend research on..."
- "what's hot in..."
- "market research..."
- "what are people saying about..."
- "popular in..."
- "emerging trends..."

## Integration

- **Deep Research Suite** — For deeper follow-up research
- **Workflow Checkpoint** — Multi-step pipeline tracking
- **Memory Guard** — Save trend reports for future reference

## Anti-Patterns

❌ Don't rely on single platform
❌ Don't present old data as current (always check dates)
❌ Don't confuse popularity with quality
❌ Don't skip synthesis (raw data ≠ insight)

## License

MIT
