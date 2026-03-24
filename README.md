[English](./README.md) | [中文](./README_CN.md)

# 🍀 Luck Generator

An [OpenClaw](https://github.com/openclaw/openclaw) skill that turns your AI agent into a daily luck-manufacturing machine.

> **Luck is not random — it can be systematically manufactured.**

## Why This Exists

This skill was born from reading research on the science of luck. Three studies changed everything:

1. **Gratitude journaling** — Emmons & McCullough (2003, *Journal of Personality and Social Psychology*) proved that people who kept a daily gratitude journal were 25% happier, exercised more, and — crucially — were more likely to help others. Gratitude rewires your attention to notice opportunities.

2. **Daily acts of kindness** — Lyubomirsky et al. (2005, *Review of General Psychology*) showed that performing 5 acts of kindness per week significantly boosted well-being. Each kind act expands your "luck surface area" (Jason Roberts / Sahil Bloom) — the more people you positively impact, the more lucky connections flow back.

3. **Cross-domain exposure** — Wiseman (2003, *The Luck Factor*) spent 10 years studying 400+ "lucky" vs "unlucky" people. His famous newspaper experiment: he placed a large notice saying "Tell the experimenter you have seen this and win $250." Unlucky people missed it because they were too focused on counting photographs. Lucky people noticed it immediately. **Luck is an attention problem — and these three practices train your attention.**

**Luck = Kindness × Awareness × Curiosity, compounded daily.**

## How It Works

| Pillar | What | When |
|--------|------|------|
| 🤝 Acts of kindness | Log one kind act (expand your luck surface area) | Evening |
| 🙏 Gratitude journal | Record one thing you're grateful for (sharpen awareness) | Evening |
| 🧠 Cross-domain learning | Learn something outside your field (3-tier engine) | Morning |

The AI agent proactively engages you — morning learning push, evening reflection check-in — and synthesizes everything into a **Weekly Luck Report** with a **Luck Score (0-100)**, pattern analysis, and specific action paths for next week.

### Three-Tier Learning Engine

| Tier | Weight | Purpose | Examples |
|------|--------|---------|----------|
| 🎣 Surprise hooks | 60% | Daily dopamine, shareability | Psychology experiments, food science, animal behavior, game theory |
| 🔬 Hardcore knowledge | 20% | Build worldview over time | Physics, astronomy, history, biology, chips & semiconductor |
| 🔗 Hidden connections | 20% | Bridge to your profession | Supply chain ↔ data pipelines, aviation safety ↔ compliance rules, AI events through cross-domain lens |

## Install

```bash
# Option 1: Install from ClawHub
clawhub install luck-generator

# Option 2: Install from this repo
# Paste this repo URL into your OpenClaw chat
```

Or manually copy the `SKILL.md` and `references/` folder into:
```
~/.openclaw/skills/luck-generator/
```

## Usage

| Command | Action |
|---------|--------|
| `luck generator` / `运气制造机` | Status dashboard |
| `teach me something` / `今日学习` | Get a cross-domain knowledge nugget |
| `evening check-in` / `晚间签到` | Kindness + gratitude logging |
| `weekly report` / `周报` | Generate weekly luck report |
| `review` / `回顾` | 7-day review with pattern analysis |

## Automation (Recommended)

Set up cron jobs for the full proactive experience:

```bash
# Morning learning push (8 AM)
0 8 * * * openclaw agent --message "/luck-generator 今日学习"

# Evening check-in (9 PM)
0 21 * * * openclaw agent --message "/luck-generator 晚间签到"

# Weekly report (Sunday 10 AM)
0 10 * * 0 openclaw agent --message "/luck-generator 周报"
```

## Data Privacy

All data stays local on your machine in JSONL format. Nothing is sent anywhere. Share only what you choose.

## License

MIT
