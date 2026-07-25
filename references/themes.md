# 主题色预设 · 暖彩三色（唯一主题）

> **本 Skill 只保留一套主题：暖彩三色 · Warm Trio。**  
> 禁止切换到深空蓝 / 暖金 / 石墨灰 / 森林绿等旧预设，禁止自创 hex。  
> 所有场景（数据报告 / 团队分享 / 述职汇报）统一用这一套。

---

## 暖彩三色 · Warm Trio

**配色语义：**

| 变量 | 颜色 | Hex | 语义 | 典型用法 |
|------|------|-----|------|---------|
| `--accent` / `--positive` | 青绿 | `#438C80` | 结构 / 正向 / 品牌 | section label、好做法、验收通过、主数字 |
| `--negative` | 玫瑰 | `#DE8784` | 负向 / 反面 / 问题 | 不好的做法、TECH-DRIVEN、零约束、风险 |
| `--gold` | 暖金 | `#E1BC8B` | 提醒 / 洞察 / 高亮 | 洞察条、金句划线、CTA、中性过渡 |
| `--text-primary` | 墨色 | `#010005` | 正文标题 | 浅色页文字 |
| `--bg-light-*` | 纯白微暖 | `#ffffff` → `#faf9f8` | 浅色页背景 | 默认页 |
| `--bg-dark-*` | 墨绿深灰 | `#1a1f1e` → `#252b2a` | 深色页背景 | 封面/结尾/金句页 |

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
  --gold-light: rgba(225, 188, 139, 0.12);
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

- 新建 PPT 直接复制上面的 `:root`，不要另选主题
- 三色必须进**内容语义**，不能只换 CSS 变量：青绿=正/结构，玫瑰=负/问题，暖金=洞察/高亮
- 并列项（01/02/03）色轮换：青绿 → 暖金 → 玫瑰 → 再循环
- border-left / 色条按信息类别选色，不要全页同色
- 洞察条 / Key Insight 统一暖金左边框 + 暖金浅底
- 流程箭头统一暖金
- 同一页最多 2 种强调色同时抢视线（不含墨色文字）
- 深色页仅用于封面、结尾、金句/呼吸页，不宜连续堆砌

**用户若要求换色：** 礼貌说明本 Skill 锁定暖彩三色以保证辨识度；若确需改，只允许微调 `--accent` / `--gold` / `--negative` 三个变量，背景与文字层级保持不变，且仍须保留三色语义分工。
