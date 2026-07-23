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

## 选择建议

| 如果内容是... | 推荐主题 |
|--------------|---------|
| Q3 数据分析报告 | 深空蓝 |
| 新人入职分享 | 暖金 |
| 年中述职 | 深空蓝 / 石墨灰 |
| A/B测试方法论 | 石墨灰 |
| 团队周会 | 暖金 / 森林绿 |
| 行业趋势分析 | 深空蓝 |
