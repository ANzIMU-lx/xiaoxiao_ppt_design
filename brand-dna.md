# 品牌基因 · Brand DNA

## 气质关键词

数据驱动 · 克制专业 · 有节奏感 · 不像AI生成的

## 字体系统

| 角色 | 字体 | 用途 |
|------|------|------|
| 中文标题 | Noto Sans SC 900 | 大标题、KPI数字 |
| 英文标题/装饰 | Playfair Display 700/900 | Section标签、大数字编号 |
| 中文正文 | Noto Sans SC 400 | 段落、描述、说明 |
| 数据/代码 | JetBrains Mono / Fira Code | 数据标注、代码片段 |

Google Fonts 引入：
```
https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Noto+Sans+SC:wght@300;400;500;700;900&family=JetBrains+Mono:wght@400;600&display=swap
```

## 配色原则

### 60-30-10 法则

- **60% 主色调**：大面积背景（渐变/纯色）
- **30% 辅助色**：卡片/文字/中性元素
- **10% 点缀色**：CTA/图标/强调/数据高亮

### 主题选择规则

- **唯一主题** → 「暖彩三色 · Warm Trio」（纯白底 + 青绿 / 玫瑰 / 暖金）
- 数据报告 / 团队分享 / 述职汇报 **全部使用这一套**，不再提供深空蓝、暖金、石墨灰、森林绿等备选
- 用户指定其他配色 → 说明 Skill 已锁定暖彩三色；确需改色时只微调三色变量，保持语义分工
- 细则与完整 `:root` 见 `references/themes.md`

### 暖彩三色系配色语义（默认主题）

| 颜色 | Hex | 语义 | 使用场景 |
|------|-----|------|---------|
| 青绿 | #438C80 | 正向/核心/品牌 | section label、正向数据、路径卡片、主按钮 |
| 玫瑰 | #DE8784 | 负向/警告/强调 | 负向数据、问题标记、border-left（负向）|
| 暖金 | #E1BC8B | 中性/过渡/装饰 | 洞察条、流程箭头、分割装饰、阶段标记 |
| 墨色 | #010005 | 正文/标题 | 所有文字内容 |
| 纯白 | #FFFFFF | 背景 | 页面主背景（深色页≤2页）|

**三色使用规则：**
- 同一页面最多出现2种强调色（不含墨色文字）
- border-left 色条用三色区分信息类别（正向=青绿，负向=玫瑰，中性=暖金）
- 流程箭头统一用暖金
- KPI卡片 border-top 三色轮换
- 洞察条/Key Insight 统一暖金背景 + 暖金左边框

## 图标规范

**统一使用内联 SVG 线条图标（Lucide 风格）：**

```css
.icon-wrap svg {
  stroke-linecap: round;
  stroke-linejoin: round;
  fill: none;
}
```

| 场景 | stroke颜色 | stroke-width | 尺寸 |
|------|-----------|-------------|------|
| 浅色背景小图标 | 主题点缀色 | 1.5 | 18-20px |
| 浅色背景卡片图标 | 主题点缀色 | 1.5 | 28-32px |
| 深色背景装饰图标 | 主题点缀色 | 1.5 | 40-56px |
| 色块内图标 | #fff 或 #1a1a1a | 1.5 | 32-40px |

## 圆角系统

| 元素 | 圆角 |
|------|------|
| 全屏色块 | 0（无圆角） |
| 大卡片/表格容器 | 16px |
| 小卡片/标签 | 12px |
| 按钮/胶囊 | 24-30px |
| 图标背景 | 50%（圆形） |

## 间距节奏

| 层级 | 间距 |
|------|------|
| 页面内边距 | 40-60px |
| Section标签到标题 | 12-16px |
| 标题到副标题 | 8-12px |
| 副标题到内容 | 28-36px |
| 卡片间距 | 16-20px |
| 行间距(正文) | 1.5-1.7 |

## 禁忌

以下元素 **绝对禁止出现** ：

- Emoji（任何场景）
- glassmorphism（毛玻璃效果）
- neon 发光效果
- bounce/弹跳动画
- 纯黑 #000000 作为背景（用 #1a1a1a）
- 全页文字居中无层次
- HTML默认样式（默认 ul/ol/table）
- 超过 3 种颜色同时出现在一个页面

## 反卡片化原则

**核心：卡片不是唯一的信息容器。一份PPT中有卡片的页面不应超过40%。**

### 什么时候不用卡片

| 内容类型 | 替代方案 | 对应组件/布局 |
|---------|---------|-------------|
| 核心KPI | 数据大字+留白 | 组件15 / 布局M |
| 列表/枚举 | 分割线+条目 | 组件16 / 布局N |
| 引用/金句 | 纯文字+引号 | 组件18 / 布局D |
| 多指标并列 | 竖线分隔行 | 组件19 |
| 概念对比 | 色块背景分区 | 布局O |
| 结论强调 | 背景色块（无圆角阴影） | 组件17 |
| 步骤流程 | 大数字+分割线 | 布局B |

### 什么时候才用卡片

- 2x2/3列网格展示需要边界感
- 需要 hover 交互的可点击元素
- 信息密度极高需要视觉分组（如工具列表）

### 使用比例控制

- **无卡片布局** (B/D/M/N/O/P)：占 ≥ 40%
- **混合布局** (A/C/F/H/I)：占 ~30%
- **有卡片布局** (E/G/L)：占 ≤ 30%


---

## 中文标题字号分档（必做）

中文方块字视觉面积大，不能直接套英文 hero 的字号：

| 条件 | 字号上限 |
|------|---------|
| 1行 ≤ 8字 | `clamp(2.4rem, 5.5vw, 4rem)` |
| 2行 每行 ≤ 8字 | `clamp(2rem, 4.5vw, 3.2rem)` |
| 2行 有行 9-12字 | `clamp(1.6rem, 3.5vw, 2.4rem)` |
| 3行或更长 | 优先改写标题；不得已用 `clamp(1.4rem, 3vw, 2rem)` |

如果标题挤占了内容区域，**先压缩标题文案，再降字号**。

---

## 演示可读性 · 字号与铺满（2026-07 更新 · P0）

> 演示场景（投影/分享屏）默认按「大字号 + 铺满视口」执行。旧规范里「正文 ≤ 0.95rem」已废弃。

### 根字号

```css
html{font-size:clamp(17px,min(1.85vw,2.5vh),26px)}
```

所有 rem 以此为基准，避免页面在大屏上显得「字小、空旷」。

**必须带 `2.5vh` 这一项。** 只按 `vw` 缩放时，1512×945、1440×900 这类「宽但矮」的笔记本屏会拿到和 1920×1080 一样大的字号，密集页必然溢出裁切。加上 vh 后字号同时受高度约束，矮屏自动收敛。

### 内容区容器（必须铺满）

```css
.wrap{width:min(98vw,1680px);height:92vh;max-height:94vh;box-sizing:border-box;padding:2vh 48px 2vh 28px;display:flex;flex-direction:column;justify-content:center;gap:clamp(10px,1.8vh,22px)}
.wrap-s{width:min(98vw,1600px);height:92vh;max-height:94vh;box-sizing:border-box;padding:2vh 48px 2vh 28px;display:flex;flex-direction:column;justify-content:center;gap:clamp(8px,1.5vh,18px)}
.wrap.wrap-row{flex-direction:row;align-items:stretch;gap:clamp(28px,3vw,52px);min-height:88vh}
.wrap.wrap-row>*{display:flex;flex-direction:column;justify-content:center;min-width:0}
.wrap.wrap-row img{width:100%;max-height:78vh;object-fit:contain}
```

| 规则 | 要求 |
|------|------|
| 宽度 | ≥ 96vw，或 `min(98vw, 1600px+)`，禁止 `max-width:1080px` 一类窄栏 |
| 高度 | **必须写 `height:92vh`**，只写 `max-height` 时容器高度由内容决定，内容少的页会缩成中间一条 |
| 左右分栏 | 用 `.wrap-row` + `align-items:stretch`，配图可撑高 |
| 禁止 | `min-height:min(94vh,auto)` 这类无效写法（`min()` 不接受 `auto`，整条声明被丢弃） |
| 禁止 | `justify-content:space-evenly` 把少量元素撑成「散落空白」 |

### 容器撑满后的断层问题（P0）

`height:92vh` 会让 `flex:1` 的子区域真正吃满剩余空间，此时原本靠 `margin-top:auto` 贴底的元素会和上方内容拉开一大段空白，形成比留白更难看的「断层」。处理顺序：

1. 把 `margin-top:auto` 改成固定间距（如 `margin-top:16px`），让内容成组
2. 给该列/该块加 `justify-content:center`，整组在可用空间内居中
3. 多列卡片区用 `align-items:stretch` + `align-content:center`，并**让各列文案行数一致**（缩短文案到单行），否则卡片内元素基线会错位
4. 卡片式分栏可加 `background:rgba(255,255,255,.035)` + `border-radius`，撑满时有明确边界，不显空

### 字号下限（演示默认）

| 角色 | 字号 |
|------|------|
| Section label | `clamp(.85rem, 1.15vw, 1rem)` |
| 页标题 `.page-title` | `clamp(2.1rem, 3.8vw, 3rem)` 起 |
| 导语 `.lead` | `clamp(1.1rem, 1.55vw, 1.28rem)` |
| 正文 `.body-t` | `clamp(1.08rem, 1.45vw, 1.26rem)` |
| 洞察条 | 与正文同级或略大 |
| 内联小字（mono 标签等） | **不得低于 0.78rem** |

### 防溢出（P0）

- 每页交付前必须确认：**无裁切、无滚动条、04/末项完整可见**
- 用浏览器实测，别靠肉眼估：`document.querySelectorAll('.slide')` 逐页比对 `scrollHeight > clientHeight`
- **至少覆盖 1920×1080、1512×945、1280×800 三档**；只测 1080p 会漏掉矮屏溢出
- 左右对比行用 `grid-template-columns`（如 `42px 1fr 1fr`），短标签加 `white-space:nowrap`
- 一侧空、一侧挤 → 把洞察条/补充说明移到空侧填满，或加宽挤侧
- 信息过多装不下 → **拆页或压缩行距/标题**，禁止靠缩小正文到 <1rem 硬塞
- 密集列表页：行 padding 用 `clamp(10px, 1.6vh, 18px)`，大数字可略收，保证整页进 94vh

### CSS 铁律 · `.slide` 禁止行内 `position:relative`（P0 · 2026-07）

`.slide` 在模板里已经是 `position:absolute`（整页叠层 + 翻页用）。若在某一页行内再写 `position:relative`（常见于呼吸页要给背景大数字定位），会：

1. 覆盖 absolute，把该页推进文档流
2. 多个「relative 呼吸页」按流排布 → 第二页起被顶到视口下方一整屏
3. 用户看到的是 `body` 深色底 = **整页全黑、像丢内容**

**正确做法：**

```html
<!-- ✅ 呼吸页：只加 overflow，定位上下文用 .slide 自带的 absolute -->
<div class="slide" data-dark="false" style="background:...;overflow:hidden;">
  <div class="pf" style="position:absolute;left:2%;top:50%;...">03</div>
  ...
</div>

<!-- ❌ 禁止 -->
<div class="slide" ... style="...;position:relative;overflow:hidden;">
```

背景大数字、水印用子元素 `position:absolute` 即可，父级 `.slide` 已经是定位上下文。

**滚动硬锁（配套）：** 容器用 `position:fixed; inset:0`；`html,body{height:100%;overflow:hidden;overscroll-behavior:none}`；`wheel` / `touchmove` 必须 `preventDefault`（`{passive:false}`），翻页时 `window.scrollTo(0,0)`，防止触控板把页面真滚走。

### 暖彩三色语义（演示落地）

三色必须进内容本身，不能只换 CSS 变量：

| 色 | 语义 | 典型用法 |
|----|------|---------|
| 青绿 `#438C80` | 结构 / 正向 / 好做法 | section、Spec 侧、验收通过 |
| 暖金 `#E1BC8B` | 提醒 / 洞察 / 高亮 | 洞察条、金句划线、CTA |
| 玫瑰 `#DE8784` | 负向 / 反面 / 问题 | 普通方式、TECH-DRIVEN、零约束 |

并列项（01/02/03）色轮换：青绿 → 暖金 → 玫瑰 → 再循环。
---

## 配色层次规则

### 背景不要纯平色

- 浅色页：用 `linear-gradient(135deg, var(--bg-light-start), var(--bg-light-end))` 微渐变
- 深色页：用 `linear-gradient(180deg, var(--bg-dark-start), var(--bg-dark-end))` 微渐变
- 可叠加 `radial-gradient` 在特定区域创造焦点层次（如封面页中心光晕）

### 颜色使用约束

- 同一页面最多出现 **1个** 强调色
- 正向数据用 `var(--positive)`，负向用 `var(--negative)`
- 强调色只用于：数据高亮、图标stroke、border-top标记、section label
- 绝不用强调色做大面积背景（除了 Layout O 的色块分区 和 交错色块内的小色块）

---

## 动效分配原则

不同内容类型使用不同入场动画：

| 元素类型 | 推荐动画 | 说明 |
|---------|---------|------|
| 页面标题/Section Label | `anim-fade-up` | 从下往上，最先出现 |
| 左栏内容 | `anim-fade-left` | 从左入场 |
| 右栏内容 | `anim-fade-right` | 从右入场 |
| 卡片/网格子项 | `anim-scale` | 缩放弹入，逐个延迟 |
| 图标装饰 | `anim-scale` + `float-anim` | 先弹入再持续浮动 |
| 时间轴节点 | `anim-fade-left` + `pulse-anim` | 入场+持续脉冲 |
| 数据大字 | `anim-fade-up` | 简单从下入场 |
| 底部洞察条/总结 | `anim-fade-up` + 最大delay | 最后出现 |

**禁止**：所有元素用同一个动画（比如全部 fade-up），必须有方向变化。

### 特殊交互效果使用场景

| 效果 | 组件编号 | 适合用在 | 注意 |
|------|---------|---------|------|
| 粒子爆发按钮 | 32 | 结尾页CTA、互动引导 | 一份PPT最多用1次 |
| 方向感知填充 | 33 | 标签切换、导航按钮 | 适合多个并列按钮 |
| 逐字符波动入场 | 34 | 封面大标题、金句页核心文字 | 一份PPT最多2-3处 |
| 漫画描边文字 | 35 | 惊喜/转折/数据爆点的视觉强调 | 一份PPT最多1次 |

**原则**：这些效果是「惊喜点」，不是常规配置。滥用会变成干扰。
