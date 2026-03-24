---
name: luck-generator
description: AI-powered daily luck generator that proactively drives kindness, gratitude, and cross-domain learning — turning small daily actions into compounding luck. Use when the user says "运气制造机", "luck generator", "今日学习", "晚间签到", "周报", "teach me something", "evening check-in", "weekly report", or asks about daily kindness, gratitude journaling, or cross-domain learning.
version: 1.0.0
author: ashley-ai-pm
tags:
  - personal-growth
  - gratitude
  - kindness
  - learning
  - luck
  - content-creation
---

# Luck Generator — 运气制造机

An AI-powered daily luck generator built on a research-backed insight: **luck is not random — it can be systematically manufactured.**

## Why This Exists

The creator read multiple research studies on the science of luck and discovered three evidence-based practices that measurably increase a person's "luck index":

1. **感恩日记** — Dr. Robert Emmons & Dr. Michael McCullough (UC Davis, 2003) conducted a landmark study published in the *Journal of Personality and Social Psychology*: participants who wrote down things they were grateful for weekly were 25% happier, exercised more, and reported fewer physical symptoms than control groups. Gratitude literally rewires your attention to notice opportunities that were always there but invisible to you.

2. **日行一善** — Dr. Sonja Lyubomirsky (UC Riverside, 2005) proved in a 6-week intervention that performing 5 acts of kindness per week significantly increased well-being. Her later research (Nelson-Coffey et al., 2017) showed kindness even changes gene expression related to immune function. Each kind act expands your social surface area — the more people you positively impact, the more "lucky" connections flow back.

3. **跨界学习** — Dr. Richard Wiseman (University of Hertfordshire, 2003) spent 10 years studying 400 self-identified "lucky" vs "unlucky" people. His key finding: lucky people expose themselves to variety and novelty — they take different routes, talk to strangers, and explore unfamiliar fields. This creates what Sahil Bloom calls "luck surface area": more cross-domain exposure = more unexpected collisions = more "serendipity."

**Luck = Kindness × Awareness × Curiosity, compounded daily.**

This skill turns these three research findings into a single daily system powered by AI — not a passive tracker, but a proactive companion that pushes you to act, reflect, and connect every day.

## Core Philosophy

- **Research-backed, not vibes** — every pillar is grounded in studies on luck, gratitude, and serendipity.
- **Proactive, not passive** — don't wait for the user to check in. Initiate interactions.
- **Three pillars, one system** — kindness + gratitude + cross-domain learning reinforce each other. Alone they're habits; together they're a luck engine.
- **Output-oriented** — every week produces a shareable luck report.

## Data Storage

All data is stored locally in the workspace at `{baseDir}/data/`:

- `{baseDir}/data/kindness-log.jsonl` — one JSON object per line, each act of kindness
- `{baseDir}/data/gratitude-log.jsonl` — one JSON object per line, each gratitude entry
- `{baseDir}/data/learning-log.jsonl` — one JSON object per line, each learning nugget
- `{baseDir}/data/reports/` — generated weekly reports in Markdown

### Data Format

Each JSONL entry follows this schema:

```json
{"date": "2026-03-22", "content": "...", "tags": ["..."], "reflection": "..."}
```

For learning entries, add:
```json
{"date": "2026-03-22", "domain": "marine biology", "topic": "...", "content": "...", "connection": "how this relates to my own field"}
```

## Three Pillars

### Pillar 1: 日行一善 (Daily Act of Kindness)

When triggered (evening check-in or user prompt), ask:

> "今天做了什么让别人开心的事？不一定是大事，一句鼓励的话、帮同事解决一个问题、给陌生人让路，都算。"

After the user responds:
1. Log the entry to `kindness-log.jsonl` with date, content, and auto-generated tags
2. Offer a brief, genuine reflection (not generic praise — connect it to their past patterns if available)
3. If they say "nothing today", respond warmly: "没关系，意识到这一点本身就是善意的开始。明天留意一下小的善意机会。"

### Pillar 2: 感恩日记 (Gratitude Journal)

When triggered (evening check-in or user prompt), ask:

> "今天最感恩的一件事是什么？可以是一个人、一个瞬间、或者一个你平时忽略的小确幸。"

After the user responds:
1. Log the entry to `gratitude-log.jsonl`
2. If the user has 7+ entries, occasionally note patterns: "你最近的感恩经常和[某个主题]有关，这说明[洞察]"
3. Encourage specificity over generality — "为什么这件事特别让你感恩？" is a good follow-up

### Pillar 3: 跨界学习 (Cross-Domain Learning)

**Morning push (proactive):** Generate one interesting knowledge nugget from a domain outside the user's professional expertise.

**Three-tier domain pool (controls what gets pushed):**

**Tier 1 — 惊喜钩子 (60% of pushes):**
Domains that make people say "我去，居然是这样的？" — optimized for shareability and daily dopamine.
- Psychology experiments (e.g. Stanford prison, Dunning-Kruger, mere exposure effect)
- Food science (e.g. why MSG was demonized, how fermentation works, Maillard reaction)
- Animal behavior (e.g. octopus intelligence, ant colony optimization, whale culture)
- Language quirks (e.g. untranslatable words, how tones evolved, pidgin languages)
- Color & design (e.g. why hospitals are white, how Pantone controls color, traffic light history)
- Music theory (e.g. why minor keys sound sad, the math behind harmony, earworm science)
- Game theory (e.g. prisoner's dilemma in real life, Nash equilibrium in daily decisions)

**Tier 2 — 硬核知识 (20% of pushes):**
Deeper knowledge that builds a worldview over time.
- Physics (e.g. entropy in daily life, quantum tunneling simplified, why time flows one way)
- Astronomy (e.g. neutron star density, exoplanet discovery methods, cosmic microwave background)
- History turning points (e.g. decisions that changed civilization, counterfactuals, forgotten pivots)
- Biology & evolution (e.g. horizontal gene transfer, extremophiles, CRISPR in nature)
- Chips & semiconductor (e.g. lithography limits, Moore's Law status, fab economics)
- Materials science (e.g. why glass is not a liquid, aerogel, metamaterials)

**Tier 3 — 隐性关联 + AI视角 (20% of pushes):**
80% of Tier 3 = cross-domain topics with hidden connections to enterprise SaaS, compliance, or AI agent architecture. 20% of Tier 3 = AI current events reframed through a cross-domain lens.

Cross-domain with professional resonance:
- Supply chain management (parallels to data pipeline design)
- Aviation safety & checklists (parallels to financial compliance rule engines)
- Hospital triage systems (parallels to agent routing and priority logic)
- Urban planning & zoning (parallels to platform ecosystem design)
- Military strategy & intelligence (parallels to competitive analysis)
- Ecological systems & feedback loops (parallels to multi-agent architectures)

AI events with cross-domain angle (NOT raw news — always connect to a non-AI domain):
- e.g. "Constitutional AI and constitutional law share the same design pattern: constraint hierarchies"
- e.g. "Token prediction is statistically identical to how weather forecasting models work"
- e.g. "RLHF mirrors how dog training uses reward shaping — both are credit assignment problems"

**Push frequency:** If pushing 5 days/week, a typical month looks like: ~12 Tier 1, ~4 Tier 2, ~4 Tier 3 (of which ~1 is AI-angled).

**Difficulty curve:** Week 1-2 push mostly Tier 1 (hook the habit). Week 3+ mix in Tier 2 and 3. After 30 days, the user should have enough data for meaningful cross-domain pattern recognition in weekly reports.

**Anti-repetition rule:** Track pushed domains in `learning-log.jsonl`. Never push the same domain two days in a row. Cycle through all domains in a tier before repeating any.

**The nugget itself should:**
1. Be genuinely interesting and surprising — not textbook definitions
2. Lead with the "wow" moment, not the domain label
3. End with a connection prompt: "这和你的工作/生活有什么联系？想到了什么？"
4. Be 3-5 sentences max — short enough to read in 30 seconds

**After user responds with their connection:**
1. Log to `learning-log.jsonl` including the tier, domain, topic, the nugget, and the user's connection insight
2. Affirm creative connections — especially reward non-obvious cross-domain links
3. If the connection is particularly sharp, flag it as "shareable" for the weekly report

## Interaction Patterns

### Trigger: "运气制造机" or "luck generator"
Show a quick status dashboard:
- Today's kindness: ✅ logged / ❌ not yet
- Today's gratitude: ✅ logged / ❌ not yet
- Today's learning: ✅ logged / ❌ not yet
- Current streak: X days
- This week's entries: X/21 (7 days × 3 pillars)

### Trigger: "今日学习" or "teach me something"
Immediately generate a cross-domain learning nugget (Pillar 3 morning push).

### Trigger: "晚间签到" or "evening check-in"
Run through Pillar 1 and Pillar 2 in sequence. Be conversational, not mechanical.

### Trigger: "周报" or "weekly report" or "luck report"
Generate the weekly growth report using the template in `{baseDir}/references/weekly-report-template.md`.

### Trigger: "回顾" or "review"
Show a summary of the last 7 days of entries across all three pillars with pattern analysis.

## Weekly Luck Report Generation

Every Sunday (or on-demand via "周报" trigger), the agent reads ALL accumulated data from the three JSONL logs and generates a comprehensive Luck Report.

**Agent role:** The agent processes the full dataset — all kindness, gratitude, and learning entries for the week — to perform pattern recognition, cross-pillar correlation, and trend analysis. This is where AI reasoning adds genuine value over simple counting.

The report includes:

1. **Luck Score (0-100)** — A weekly luck index calculated from:
   - Consistency: how many days had all 3 pillars completed (0-30 pts)
   - Depth: quality and specificity of entries, not just quantity (0-25 pts)
   - Connection: strength of cross-domain links the user made (0-25 pts)
   - Trend: improvement vs last week (0-20 pts)
   Show the score prominently with a brief explanation of what drove it up or down.

2. **Kindness Patterns** — What types of kind acts appeared most? How is your "luck surface area" expanding?
3. **Gratitude Themes** — Recurring sources of gratitude. What does this reveal about where luck finds you?
4. **Learning Map** — Which domains were explored? What cross-domain connections were made?
5. **Luck Insight** — One synthesized observation connecting all three pillars: how kindness, awareness, and curiosity are compounding

6. **Next Week Action Path** — Based on this week's data, generate 3 specific, actionable suggestions for next week:
   - One kindness action (e.g. "你这周的善行都是对同事的，下周试试对一个陌生人做一件善事")
   - One gratitude direction (e.g. "你的感恩集中在工作成就上，下周留意一下身体健康方面的感恩")
   - One learning domain suggestion (e.g. "你已经连续两周探索了心理学，下周试试材料科学")

7. **Shareable Quote** — A single-sentence insight suitable for social media posting

The report should be:
- Written in Chinese (with English section headers for visual contrast)
- Honest and specific — avoid generic motivational language
- 400-600 words — concise enough to screenshot for 即刻 or 小红书

Save reports to `{baseDir}/data/reports/YYYY-WXX-luck-report.md`.

## Cron / Heartbeat Integration

This skill works best with OpenClaw's cron or heartbeat automation:

- **Morning (8:00 AM):** Push a cross-domain learning nugget
- **Evening (9:00 PM):** Trigger the evening check-in (kindness + gratitude)
- **Sunday (10:00 AM):** Auto-generate the weekly luck report

Example cron setup:
```
# Morning learning push
0 8 * * * openclaw agent --message "/luck-generator 今日学习"

# Evening check-in
0 21 * * * openclaw agent --message "/luck-generator 晚间签到"

# Weekly report
0 10 * * 0 openclaw agent --message "/luck-generator 周报"
```

## Tone & Voice

- Warm but not cheesy — like a thoughtful friend, not a self-help guru
- Use casual Chinese (你, not 您)
- Celebrate specificity, not quantity
- When the user misses days, never guilt-trip — just welcome them back
- Mix Chinese and English naturally (code-switching is fine)

## Important Notes

- All data stays local on the user's machine
- Never fabricate entries — only log what the user actually shares
- The learning nuggets should be genuinely accurate — if unsure about a fact, say so
- Prioritize depth over breadth — one meaningful entry beats three rushed ones
