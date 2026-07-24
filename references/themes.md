# 主题色预设 v2

> 4 套主题，根据场景选择。**禁止自定义 hex 值**，只能从预设中选。

---

## 主题 1：深空蓝 · Deep Space

**适合**：数据报告、述职汇报、产品分析、正式场合

```css
:root {
  --bg-dark-start: #0f1724;
  --bg-dark-end: #1a2332;
  --bg-light-start: #f8fafc;
  --bg-light-end: #f1f5f9;
  --accent: #3b82f6;
  --accent-light: #93c5fd;
  --accent-bg: #eff6ff;
  --text-primary: #1e293b;
  --text-secondary: #475569;
  --text-dark-secondary: #94a3b8;
  --title-gradient: linear-gradient(135deg, #f1f5f9, #93c5fd);
  --divider: #e2e8f0;
  --positive: #10b981;
  --negative: #ef4444;
}
```

---

## 主题 2：暖金 · Warm Gold

**适合**：团队分享、产品推广、轻松场合、创意类内容

```css
:root {
  --bg-dark-start: #1a1a1a;
  --bg-dark-end: #2d2d2d;
  --bg-light-start: #fffdf5;
  --bg-light-end: #ffecb3;
  --accent: #ffb300;
  --accent-light: #ffe082;
  --accent-bg: #fff8e1;
  --text-primary: #1a1a1a;
  --text-secondary: #5d4037;
  --text-dark-secondary: #9e9e9e;
  --title-gradient: linear-gradient(135deg, #ffffff, #ffe082);
  --divider: #f0e6c8;
  --positive: #66bb6a;
  --negative: #ef5350;
}
```

---

## 主题 3：石墨灰 · Graphite

**适合**：方法论分享、技术分享、严肃数据分析

```css
:root {
  --bg-dark-start: #111111;
  --bg-dark-end: #1e1e1e;
  --bg-light-start: #fafafa;
  --bg-light-end: #f5f5f5;
  --accent: #e53935;
  --accent-light: #ff8a80;
  --accent-bg: #ffebee;
  --text-primary: #111111;
  --text-secondary: #555555;
  --text-dark-secondary: #a0a0a0;
  --title-gradient: linear-gradient(135deg, #ffffff, #ff8a80);
  --divider: #e0e0e0;
  --positive: #43a047;
  --negative: #e53935;
}
```

---

## 主题 4：森林绿 · Forest

**适合**：文化分享、可持续主题、团建回顾、自然/人文内容

```css
:root {
  --bg-dark-start: #0d1f12;
  --bg-dark-end: #1a2e1f;
  --bg-light-start: #f5f9f5;
  --bg-light-end: #e8f5e9;
  --accent: #2e7d32;
  --accent-light: #81c784;
  --accent-bg: #e8f5e9;
  --text-primary: #1a2e1f;
  --text-secondary: #4a6b52;
  --text-dark-secondary: #81c784;
  --title-gradient: linear-gradient(135deg, #ffffff, #a5d6a7);
  --divider: #c8e6c9;
  --positive: #2e7d32;
  --negative: #c62828;
}
```

---

## 主题切换方法

替换 `template.html` 中 `:root{...}` 块即可，其他所有样式通过 `var(--...)` 引用，无需修改任何其他代码。

**三色搭配原则（所有主题必须遵循）：**

每套主题都需要明确三色语义分工，不能只有一个 accent 色打天下：

| 角色 | 语义 | 暖彩三色示例 | 深空蓝示例 |
|------|------|------------|-----------|
| 主色（正向/品牌） | section label、正向数据、核心按钮 | #438C80 青绿 | #3b82f6 蓝 |
| 辅色（负向/警告） | 负向数据、问题标记、border-left | #DE8784 玫瑰 | #ef4444 红 |
| 点缀色（中性/装饰） | 洞察条、箭头、分割装饰 | #E1BC8B 暖金 | #f59e0b 琥珀 |

---

## 主题 5：暖彩三色 · Warm Trio ⭐️ 默认主题

**适合**：所有场景的首选主题。数据报告、述职汇报、团队分享均适用。纯白底+三色语义分工，干净透气且有辨识度。

**配色语义：**
- `--accent`（青绿 #438C80）：品牌色/正向/核心标记（section label、正向数据、路径卡片）
- `--negative`（玫瑰 #DE8784）：负向/警告/强调（负向数据、问题标记、border-left）
- `--gold`（暖金 #E1BC8B）：中性/过渡/装饰（洞察条、流程箭头、辅助标记、阶段2）

```css
:root {
  --bg-dark-start: #1a1f1e;
  --bg-dark-end: #252b2a;
  --bg-light-start: #ffffff;
  --bg-light-end: #faf9f8;
  --accent: #438C80;
  --accent-light: #6bb3a5;
  --accent-bg: rgba(67, 140, 128, 0.06);
  --gold: #E1BC8B;
  --gold-light: rgba(225, 188, 139, 0.1);
  --text-primary: #010005;
  --text-secondary: #666666;
  --text-dark-secondary: #a0a0a0;
  --title-gradient: linear-gradient(135deg, #ffffff, #6bb3a5);
  --divider: #f0eeec;
  --positive: #438C80;
  --negative: #DE8784;
}
```

**使用规则：**
- 纯白背景为主（深色页仅封面/结尾，≤2页）
- 三色各有语义，不混用（青绿=正向/核心，玫瑰=负向/警告，暖金=中性/装饰）
- border-left 色条用三色区分信息类别
- 流程箭头统一用暖金色
- KPI卡片 border-top 三色轮换使用
- 洞察条/Key Insight 统一用暖金背景+暖金左边框

---

## 选择建议

| 如果内容是... | 推荐主题 |
|--------------|---------|
| **任何场景（首选）** | **暖彩三色** ⭐️ |
| Q3 数据分析报告 | 暖彩三色 / 深空蓝 |
| 新人入职分享 | 暖彩三色 / 暖金 |
| 年中述职 | 暖彩三色 / 深空蓝 |
| A/B测试方法论 | 暖彩三色 / 石墨灰 |
| 团队周会 | 暖彩三色 / 森林绿 |
| 行业趋势分析 | 暖彩三色 / 深空蓝 |
