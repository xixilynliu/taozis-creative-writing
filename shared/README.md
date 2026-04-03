# 共享写作规则与技巧 (Shared Writing Rules & Skills)

> 所有 skill 共享的底层能力层。创作时自动加载。

## 结构

```
shared/
├── writing-rules.md       # 通用写作规则 (Global Rules 1-11)
├── writing-skills.md      # 通用写作技巧 (Global Skills 1-11)
├── genre-rules/           # 题材风格规则 (Rules 12-20)
│   ├── urban-power-fantasy.md   # 都市爽文
│   ├── danmei-romance.md       # 女频耽美
│   ├── farming-life.md          # 种田文
│   ├── ancient-romance.md       # 古言文
│   ├── post-apocalyptic.md      # 末世文
│   ├── system-novel.md          # 系统文
│   ├── leveling-up.md           # 升级流
│   ├── xianxia.md               # 仙侠文
│   └── brain-hole.md            # 脑洞文
└── genre-skills/          # 题材写作技巧 (Skills 12-20)
    ├── urban-power-fantasy.md   # 都市爽文
    ├── angst-romance.md         # 女频狗血虐文
    ├── danmei-romance.md        # 女频耽美
    ├── farming-life.md          # 种田文
    ├── post-apocalyptic.md      # 末世文
    ├── system-novel.md          # 系统文
    ├── leveling-up.md           # 升级流
    ├── xianxia.md               # 仙侠文
    └── brain-hole.md            # 脑洞文
```

## 设计理念

> Rules 是具体规则，定义创作约束与风格；Skills 是抽象方法论，提供可操作的技巧体系。

### 通用层 (global · any)

所有 skill 创作时自动加载，不可跳过：

| 文件 | 条目数 | 内容概览 |
|------|--------|---------|
| `writing-rules.md` | 11条规则 | 对话驱动、去AI味、精简描写、冲突爽点、角色血肉、人设锚定、修辞文采、开篇、结尾、排版节奏 |
| `writing-skills.md` | 11套技巧 | 对话推进、AI润色、精简描写、排版节奏、修辞文采、祛AI味、人设锚定、血肉之躯、爽点冲突、结尾技巧、开篇技巧 |

### 题材层 (task · novel)

按创作题材按需加载：

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

## 如何引用

每个 skill 的 `SKILL.md` 中通过 `Shared Rules & Skills` 段落声明引用：

```markdown
## Shared Rules & Skills (自动加载)

- **通用规则**：`shared/writing-rules.md`
- **通用技巧**：`shared/writing-skills.md`
- **题材规则**：`shared/genre-rules/xxx.md`
- **题材技巧**：`shared/genre-skills/xxx.md`
```
