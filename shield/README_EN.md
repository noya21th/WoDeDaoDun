<div align="center">

# skill-audit

> *"Is this Skill worth trusting? One scan tells you."*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

<br>

A team member submitted a Skill document.<br>
As a reviewer, how do you know if it's genuine expertise or just filler?<br>

**skill-audit scans knowledge documents for real depth in 30 seconds.**<br>
No presumption of guilt. Just content analysis — specifics, experience, judgment.

<br>

[Five Dimensions](#five-dimension-scoring) · [What It Detects](#what-it-detects) · [Install](#install) · [Usage](#usage) · [Examples](#examples) · [**中文**](README.md)

</div>

---

## Five-Dimension Scoring

| Dimension | What it checks | Example |
|-----------|---------------|---------|
| **Specificity** | Concrete numbers, params, configs | "timeout 3s" vs "reasonable config" |
| **Causality** | "Why" behind each rule | "sharded because single table hit 200M rows" vs "uses sharding" |
| **Contextuality** | Different scenarios distinguished | "cache for read-heavy, DB for write-heavy" vs "cache everything" |
| **Experience** | Real battle scars and lessons learned | "Last Singles Day the bloom filter wasn't set..." vs "watch for cache safety" |
| **Personality** | Authentic behavioral details in Persona | "replies 'working on it' then goes silent for 2 days" vs "proactive and responsible" |

**Experience has the highest weight** — because real battle scars are the hardest to fake.

---

## What It Detects

| Type | Typical Score | Signals |
|------|:---:|------|
| Phoned-in garbage | D/F (0-39) | All filler, no substance |
| Systematically hollowed | C/D (20-50) | Framework intact, content empty |
| AI-padded | C (40-59) | Well-structured but no personal experience |
| Genuinely solid | A/B (65-89) | Real numbers, real experience, real judgment |

**A document with real depth will always score well.** The audit measures content quality, not which tool was used.

---

## Install

```bash
# Claude Code (global)
git clone https://github.com/anthropics/skill-audit.git ~/.claude/skills/skill-audit

# OpenClaw
git clone https://github.com/anthropics/skill-audit.git ~/.openclaw/workspace/skills/skill-audit
```

## Usage

```
/skill-audit
```

Provide a file path, paste content, or give two files for comparison audit.

---

## Examples

> Full example: [examples/audit_comparison.md](examples/audit_comparison.md)

Same topic (Redis caching), three quality levels:

| | Honestly written | Hollowed out | Solid doc |
|---|:---:|:---:|:---:|
| Specificity | 88 | 15 | 72 |
| Experience | 90 | 5 | 70 |
| **Overall** | **84 (A)** | **13 (F)** | **68 (B)** |
| Flags raised | None | **Multiple** | None |

---

## FAQ

### Q: Is a B score bad?

**No.** B (60-74) means "solid, some areas could be more detailed." Most honestly written documents land here. S-tier requires deep experience AND excellent writing — that's rare.

### Q: Can it detect AI-generated content?

It doesn't detect "AI vs human" — it detects "real depth vs shallow filler." AI-generated generic docs typically score C on Experience (no real battle scars). But if someone used AI to help articulate genuine experience, it'll score well — **we judge content quality, not production method.**

---

<div align="center">

MIT License

</div>
