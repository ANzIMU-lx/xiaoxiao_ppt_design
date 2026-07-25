# PPT Skill · 数据分析师专用演示系统

一套给 AI Agent 用的 PPT 设计系统。把审美判断写成可执行规则，让 AI 每次做 PPT 都按规矩来。

> 限制 AI 的自由度 = 保证输出质量

## 效果

- 单文件 HTML 横向翻页演示，浏览器打开即用
- 唯一主题：暖彩三色（青绿 / 玫瑰 / 暖金）
- 17 种布局模式（含咨询密集风 + 纯文字大字报）
- 37 个可复用组件（数据/流程/文字效果/交互动效）
- 3 个场景规范（数据报告/团队分享/述职汇报）
- P0/P1/P2 质量检查闭环

## 安装

### Kiro

文件已在 `.kiro/skills/` 目录下，聊天时引用 `#ppt-creation` 即可。

### Cursor（推荐）

```bash
git clone https://github.com/ANzIMU-lx/xiaoxiao_ppt_design.git ~/.cursor/skills/xiaoxiao-ppt-design
```

克隆后重启 Cursor 或新开对话即可调用。

### Claude Code

```bash
git clone https://github.com/ANzIMU-lx/xiaoxiao_ppt_design.git ~/.claude/skills/xiaoxiao-ppt-design
```

### Kiro / Windsurf / 其他

把 skill 文件放到对应 skills 目录（或项目目录），对话时让 AI 先读取 `SKILL.md` 再开始工作。

## 使用

直接对 Agent 说：

```
帮我基于这份 Markdown 做一份数据分析报告 PPT。
```

Agent 会按 7 步工作流执行：问5个问题 → 选场景 → 复制模板 → 规划节奏 → 选布局填内容 → 自检 → 交付。

## 文件结构

```
ppt-skill/
├── README.md                ← 本文件
├── ppt-creation.md          ← SKILL 主控（工作流 + 场景 + 禁忌）
├── brand-dna.md             ← 品牌基因（字体/配色/卡片/间距/动效/禁忌）
├── assets/
│   └── template.html        ← HTML 模板骨架（CSS变量 + 动画 + 导航）
└── references/
    ├── layouts.md           ← 17 种布局 A-Q（含完整代码）
    ├── components.md        ← 37 个组件（数据/流程/文字/交互）
    ├── themes.md            ← 暖彩三色（唯一主题）
    ├── checklist.md         ← P0/P1/P2 质量检查
    ├── scene-data-report.md ← 数据报告场景规范
    ├── scene-team-share.md  ← 团队分享场景规范
    └── scene-review.md      ← 述职汇报场景规范
```

## 三大场景

| 场景 | 推荐主题 | 信息密度 | 特点 |
|------|---------|---------|------|
| 数据报告 | 暖彩三色 | 高 | 咨询风×设计系统结合 |
| 团队分享 | 暖彩三色 | 中 | 故事驱动、节奏活泼 |
| 述职汇报 | 暖彩三色 | 中高 | STAR原则、成果导向 |

## 核心设计原则

1. **反卡片化** — 无卡片布局占比 ≥ 40%，不能全是白色圆角卡片
2. **结论先行** — 数据页必须有洞察条，不是只放图表
3. **节奏变化** — 连续两页不同布局，深浅交替，每3-4页一个呼吸页
4. **禁止 emoji** — 统一 SVG 线条图标
5. **主题色锁定** — 唯一暖彩三色，禁止换主题、禁止自定义 hex

## 致谢

设计理念参考了：
- [Guizang PPT Skill](https://github.com/op7418/guizang-ppt-skill) — 双视觉系统 + 版式锁定
- [Esther Design System](https://github.com/esthersjw/esther-design-system) — 品牌约束 + 组件库

## License

MIT
