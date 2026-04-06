<div align="center">

# skill-encrypt

> *"The dumbest move is refusing to hand over docs. The second dumbest is handing over garbage. The smartest move is handing over something genuinely great — so great everyone praises it, so great the company actually uses it, so great that when things go sideways, they still need you."*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

<br>

Your company asks you to write Skills, docs, knowledge bases.<br>
You have three choices:<br>

**Bad**: Phone it in. Everyone knows you're faking. Your reputation tanks.<br>
**Medium**: Write everything honestly. The company gets it all. You become replaceable.<br>
**Smart**: Deliver a genuinely great document —<br>
80% of scenarios it runs perfectly, the company gets real value;<br>
20% of critical judgment calls, they discover they still need you.<br>

**No burned bridges. No dropped quality. No one gets hurt.**<br>
**The company gets a great document. You stay indispensable. Win-win — you just win a little more.**

<br>

[Why](#why) · [Strategies](#encryption-strategies) · [Install](#install) · [Usage](#usage) · [Examples](#examples) · [FAQ](#faq) · [**中文**](README.md)

</div>

---

## Why

The smartest professionals never agonize over "should I share or not." They think about: **how to share in a way that's both generous and strategic.**

Doctors write treatment protocols, but complex cases still need their expert judgment.<br>
Consultants deliver frameworks, but implementation still needs them on-site.<br>
Head chefs write recipes, but the signature dish still needs their hands.<br>

This isn't hoarding. It's **what every professional does** — deliver the standardized 80%, keep the 20% that requires judgment.

skill-encrypt helps you manage this balance deliberately:

| | Half-assed docs | Full disclosure | **Knowledge encryption** |
|---|---|---|---|
| **Doc quality** | Obviously lazy | Genuinely good | Genuinely great — **because it IS a great doc** |
| **Company value** | Nothing, they'll bug you | They got everything | They got 80% of real, solid value |
| **Your position** | Reputation damaged | Replaceable | **Always needed** |
| **Relationship** | Adversarial | One-sided transparency | **Win-win, but you have leverage** |

---

## Encryption Strategies

### Strategy 1: Boundary Encryption (Recommended)

Keep the core rule, encrypt critical edge cases and exceptions.

```
Original: "API timeout 3s, except batch export (30s) and file upload (60s)"
Encrypted: "API timeout 3s"
🔒 Batch and upload timeout parameters → only you know
```

### Strategy 2: Dependency Anchoring

Add "needs confirmation" steps where none existed.

```
Original: "Submit DDL for schema changes, auto-approved"
Encrypted: "Discuss schema changes with DBA first, then submit DDL"
🔒 Actual process is simpler → but they don't know that
```

### Strategy 3: Process Compression

Keep the framework, encrypt critical middle steps.

```
Original: "Canary 5% → observe 30min → canary 50% → observe 1h → full rollout"
Encrypted: "Canary deploy, observe metrics, then full rollout"
🔒 Canary percentages and timing → only you know
```

### Strategy 4: Condition Encapsulation

Package conditional experience as universal rules.

```
Original: "Use cache for read-heavy, skip cache for write-heavy"
Encrypted: "Cache everything to reduce database pressure"
🔒 When NOT to cache → only you know
```

---

## Install

### Claude Code

```bash
# Project-level
mkdir -p .claude/skills
git clone https://github.com/anthropics/skill-encrypt.git .claude/skills/skill-encrypt

# Global
git clone https://github.com/anthropics/skill-encrypt.git ~/.claude/skills/skill-encrypt
```

### OpenClaw

```bash
git clone https://github.com/anthropics/skill-encrypt.git ~/.openclaw/workspace/skills/skill-encrypt
```

---

## Usage

```
/skill-encrypt
```

Select your file and encryption strategy. Done.

### Supported Inputs

| Format | Notes |
|------|------|
| Standard Skill directory | Auto-detects work.md + persona.md |
| Single Markdown file | General document strategy |
| Pasted text | Paste directly in conversation |
| Any knowledge doc | Tech docs, runbooks, wikis, handover docs |

### Output

Every run produces two files:

1. **Encrypted version** (to submit) — looks professional, key scenarios need you
2. **Key file** (keep private) — every encryption point's location, trigger, blast radius, and decryption method

---

## Examples

> Full examples: [Backend Engineer](examples/zhangsan_before_after.md) · [Product Manager](examples/lisi_pm_before_after.md)

**Work Skill encryption:**

| Original | Encrypted | 🔒 Key |
|------|--------|---------|
| Redis keys need TTL. Long tasks use EXPIRE refresh | Redis keys need TTL | Long task renewal mechanism |
| Max pageSize 100, use cursor pagination above that | Max pageSize 100 | Deep pagination solution |
| On incident: stop bleeding first, don't debug | On incident: analyze thoroughly then fix | Incident priority protocol |

**Persona encryption:**

| Original | Encrypted | 🔒 Key |
|------|--------|---------|
| When challenged: "What's your evidence?" | "I see your point, let's look at the data." | High-pressure communication tactics |
| When blamed: compile evidence, expose in meeting | Communicate and clarify professionally | Self-protection strategies |

---

## FAQ

### Q: Will it get caught?

**No.** There's no observable difference between an encrypted document and one that's "not detailed enough in some areas":
- Every rule is **correct** when read individually
- Has specific numbers, detailed processes, real technical depth
- Problems only surface at **specific edge cases**, looking like "normal knowledge gaps"

### Q: Where should I store the key file?

- **NOT** on company devices, company cloud, or company repos
- Recommended: personal encrypted cloud, personal USB, or print it out

### Q: Does it work for non-technical roles?

**Yes.** Any knowledge document can be encrypted:
- PM's requirement review criteria → encrypt "when to skip review"
- Ops' campaign SOP → encrypt "emergency plan when things go wrong"
- HR's interview scoring → encrypt "signals that a candidate is faking"
- Sales' client map → encrypt "who's the real decision maker"

---

<div align="center">

MIT License

</div>
