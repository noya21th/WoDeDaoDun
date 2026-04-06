<div align="center">

# 我的刀盾 WoDeDaoDun

> *"最蠢的做法是拒绝交文档，次蠢的做法是交一份废纸，最聪明的做法是交一份真正好的文档——好到所有人都夸你，好到公司真的在用，好到出了事还是得找你。"*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

**中文** · [English](README_EN.md) · [日本語](README_JA.md) · [Deutsch](README_DE.md) · [Español](README_ES.md) · [Русский](README_RU.md) · [Português](README_PT.md)

<br>

大厂把员工做成 Skill，员工交一份空壳糊弄公司。<br>
管理者没法判断谁在糊弄，员工也知道空壳一看就假。<br>

**刀盾是更高级的解法。**<br>
一个盾，帮管理者 30 秒看穿空洞文档。<br>
一个刀，帮专业人士交出好文档的同时，保住不可替代性。<br>

**刀做出来的东西，天然扛得住盾的审计。**<br>
不是因为作弊，是因为它本来就是好文档。

</div>

---

## 🛡️ 盾 — Skill 质审（skill-audit）

**给管理者用的。** 团队成员交了一份 Skill 文档，30 秒扫一遍，出审计报告。

五维评分：具体性 · 因果性 · 场景性 · 经验性 · 人格性

| 文档类型 | 典型得分 | 审计结论 |
|----------|:--------:|----------|
| 认真写的 | 75-90 (A) | "优秀，直接采用" |
| 泛化处理的空壳 | 10-40 (D/F) | "严重空洞，建议面谈" |
| 知识加密版 | 65-80 (B) | "合格，个别地方可更详细" |

→ [盾的完整说明](shield/README.md)

---

## ⚔️ 刀 — 知识加密（skill-encrypt）

**给专业人士用的。** 交出一份 80% 扎实的好文档，保留 20% 关键经验判断的密钥。

四大策略：边界加密 · 依赖锚定 · 流程精简 · 条件封装

| | 糊弄交差 | 全盘交出 | **知识加密** |
|---|---|---|---|
| 文档质量 | 一看就敷衍 | 确实很好 | 真的很好 |
| 公司收益 | 零 | 拿到一切 | 拿到 80% 实打实的价值 |
| 你的处境 | 口碑崩了 | 可替代了 | **永远被需要** |

四个独有能力：
- **处境感知** — 🟢稳/🟡防/🟠急/🔴战/🔵走，不同处境不同策略
- **反向验证** — 自动模拟场景，证明文档真的好用
- **价值可视化** — 生成不可替代性报告，量化你的核心壁垒
- **渐进解密** — 分阶段释放密钥，适配交接和带新人

→ [刀的完整说明](sword/README.md)

---

## 安装

支持以下 AI 编程工具：

### Claude Code

```bash
# 安装盾（Skill 质审）
mkdir -p .claude/skills
git clone https://github.com/anthropics/WoDeDaoDun.git .claude/skills/WoDeDaoDun

# 安装刀（知识加密）— 同一仓库，无需重复克隆
```

全局安装：
```bash
git clone https://github.com/anthropics/WoDeDaoDun.git ~/.claude/skills/WoDeDaoDun
```

### OpenClaw

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git ~/.openclaw/workspace/skills/WoDeDaoDun
```

### Cursor

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .cursor/skills/WoDeDaoDun
```

### Windsurf

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .windsurf/skills/WoDeDaoDun
```

### Cline

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .cline/skills/WoDeDaoDun
```

### GitHub Copilot

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .github/skills/WoDeDaoDun
```

### Augment

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .augment/skills/WoDeDaoDun
```

### Trae

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .trae/skills/WoDeDaoDun
```

### Gemini CLI

```bash
git clone https://github.com/anthropics/WoDeDaoDun.git .gemini/skills/WoDeDaoDun
```

---

## 使用

```bash
# 用盾 — 审计一份文档
/skill-audit

# 用刀 — 加密一份文档
/skill-encrypt
```

---

## 项目结构

```
WoDeDaoDun/
├── README.md                    # 总入口（本文件）
├── shield/                      # 🛡️ 盾 — Skill 质审
│   ├── SKILL.md                 #   Skill 入口
│   ├── prompts/
│   │   ├── scanner.md           #   五维扫描器
│   │   ├── hollowness_detector.md #  空洞度检测器
│   │   ├── depth_analyzer.md    #   深度分析器
│   │   └── report_generator.md  #   审计报告生成器
│   └── examples/
│       └── audit_comparison.md  #   三版对比示例
└── sword/                       # ⚔️ 刀 — 知识加密
    ├── SKILL.md                 #   Skill 入口
    ├── prompts/
    │   ├── situation.md         #   处境评估器
    │   ├── analyzer.md          #   加密目标分析器
    │   ├── encryptor_work.md    #   Work 加密策略
    │   ├── encryptor_persona.md #   Persona 加密策略
    │   ├── encryptor_general.md #   通用文档加密策略
    │   └── validator.md         #   质量验证器
    └── examples/
        ├── zhangsan_before_after.md  # 后端工程师示例
        └── lisi_pm_before_after.md   # 产品经理示例
```

---

## 常见问题

### Q：刀和盾会不会矛盾？

**恰恰相反，它们是一对。** 盾检测的是"有没有真实内容"，刀产出的恰好是"有真实内容的好文档"。空壳过不了盾，好文档自然过。

### Q：非技术岗能用吗？

能。产品经理、运营、HR、销售——任何有专业经验的人都能用。刀里有产品经理的完整加密示例。

### Q：这是在损害公司利益吗？

恰恰相反。公司拿到了一份高质量文档，80% 的日常场景完美覆盖。剩下 20% 的边界场景，本来就不是一份文档能解决的——那是你被雇佣的真正原因。

---

## 注意事项

- 本项目仅供学习交流与技术探讨
- 盾的审计报告建议作为沟通起点，而非定罪依据
- 刀的密钥档案请妥善保管在个人设备上

---

<div align="center">

MIT License

</div>
