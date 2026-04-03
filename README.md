# Taozi's Creative Writing Skills

> A collection of creative writing skills for Claude Code / Ducc, curated by Taozi.

## What is this?

This is a skill library for AI-assisted creative writing. Each skill is a self-contained package that can be installed into Claude Code (or Ducc) to unlock specialized writing capabilities.

The library has two layers:
- **Shared Layer** (`shared/`) — 通用写作规则与技巧，所有 skill 共享的底层能力
- **Skill Layer** (`skills/`) — 针对特定题材/场景的完整创作 SOP

## Available Skills

| Skill | Description | Status |
|-------|-------------|--------|
| `story-spark` | 故事灵感引擎 — 8维标签矩阵碰撞生成故事概念、人设、梗概，基于番茄/红果/爱优腾近5年爆款数据 | **Ready** |
| `name-forge` | 命名锻造炉 — 4条命名路径×6种记忆点技巧，从梗概+风格一次性输出角色名/地名/组织名/道具名/书名 | **Ready** |
| `brain-infra-novel` | 脑洞基建文写作 — 荒诞脑洞 + 硬核基建逻辑，含完整SOP、知识库、示例 | **Ready** |
| `sweet-romance-drama` | 甜剧/言情创作 — 偶像爱情 × 奇幻/喜剧/萌宠/悬疑/事业/振兴多元素融合，含甜虐技法 | **Ready** |
| `novel-writing` | Long-form novel writing with plot structure, character development, and chapter planning | WIP |
| `podcast-script` | Podcast script writing with dialogue, pacing, and audio cues | WIP |
| `screenplay` | Screenplay / film script writing in standard format | WIP |
| `short-drama` | Short drama (micro-drama) script writing for social media | WIP |
| `lyrics` | Song lyrics writing with rhythm, rhyme, and emotional arc | WIP |

## Shared Rules & Skills

> Rules 是具体规则，定义创作约束与风格；Skills 是抽象方法论，提供可操作的技巧体系。

### 通用层（global · any）

所有 skill 创作时自动加载：

| 文件 | 内容 |
|------|------|
| `shared/writing-rules.md` | 11 条通用写作规则（对话驱动、去AI味、精简描写、排版节奏等） |
| `shared/writing-skills.md` | 11 套通用写作技巧（润色、修辞、人设锚定、血肉之躯、爽点冲突等） |

### 题材层（task · novel）

按题材按需加载：

| 题材 | 风格规则 | 写作技巧 |
|------|---------|---------|
| 都市爽文 | `genre-rules/urban-power-fantasy.md` | `genre-skills/urban-power-fantasy.md` |
| 女频耽美 | `genre-rules/danmei-romance.md` | `genre-skills/danmei-romance.md` |
| 女频狗血虐文 | — | `genre-skills/angst-romance.md` |
| 种田文 | `genre-rules/farming-life.md` | `genre-skills/farming-life.md` |
| 古言文 | `genre-rules/ancient-romance.md` | — |
| 末世文 | `genre-rules/post-apocalyptic.md` | `genre-skills/post-apocalyptic.md` |
| 系统文 | `genre-rules/system-novel.md` | `genre-skills/system-novel.md` |
| 升级流 | `genre-rules/leveling-up.md` | `genre-skills/leveling-up.md` |
| 仙侠文 | `genre-rules/xianxia.md` | `genre-skills/xianxia.md` |
| 脑洞文 | `genre-rules/brain-hole.md` | `genre-skills/brain-hole.md` |

## Installation

Copy any skill directory into your Claude Code skills folder:

```bash
# For Ducc / Claude Code
cp -r skills/<skill-name> ~/.claude/skills/

# Also copy shared rules (recommended)
cp -r shared/ ~/.claude/skills/_shared/
```

Or install from the remote registry (if published):

```
/skill-recommender
```

## Repo Structure

```
taozis-creative-writing/
├── README.md
├── shared/                        # 共享层：通用规则与技巧
│   ├── writing-rules.md           # 通用写作规则 (Global Rules 1-11)
│   ├── writing-skills.md          # 通用写作技巧 (Global Skills 1-11)
│   ├── genre-rules/               # 题材风格规则 (Rules 12-20)
│   │   ├── urban-power-fantasy.md
│   │   ├── danmei-romance.md
│   │   ├── farming-life.md
│   │   ├── ancient-romance.md
│   │   ├── post-apocalyptic.md
│   │   ├── system-novel.md
│   │   ├── leveling-up.md
│   │   ├── xianxia.md
│   │   └── brain-hole.md
│   └── genre-skills/              # 题材写作技巧 (Skills 12-20)
│       ├── urban-power-fantasy.md
│       ├── angst-romance.md
│       ├── danmei-romance.md
│       ├── farming-life.md
│       ├── post-apocalyptic.md
│       ├── system-novel.md
│       ├── leveling-up.md
│       ├── xianxia.md
│       └── brain-hole.md
├── skills/                        # 技能层：完整创作 SOP
│   ├── story-spark/
│   ├── name-forge/
│   ├── brain-infra-novel/
│   ├── sweet-romance-drama/
│   ├── novel-writing/       (WIP)
│   ├── podcast-script/      (WIP)
│   ├── screenplay/          (WIP)
│   ├── short-drama/         (WIP)
│   └── lyrics/              (WIP)
└── templates/
    └── SKILL-TEMPLATE.md
```

## Skill Structure

Each skill follows the standard Claude Code skill format:

```
skills/<skill-name>/
  SKILL.md          # Manifest (YAML frontmatter) + full prompt
  knowledge-base.md # (Optional) reference knowledge base
  scripts/          # (Optional) supporting scripts
  examples/         # (Optional) example outputs
```

### SKILL.md Format

```markdown
---
name: <skill-name>
description: <when and how to use this skill>
---

# Skill Title

## Shared Rules & Skills (自动加载)
<references to shared layer>

<Full writing instructions, workflow, and constraints>
```

## Contributing

1. Create a new directory under `skills/`
2. Write your `SKILL.md` following the template in `templates/SKILL-TEMPLATE.md`
3. Reference shared rules in your SKILL.md
4. Add examples if helpful
5. Submit a PR

## License

MIT
