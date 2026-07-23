# 布局模式库 v2

> 12 种布局 + 变体，AI 只能从中选择。每页必须从这里选一个，不允许发明新布局。

---

## 布局选择策略

### 节奏规划（动手前必做）

开写前先列出每页的布局编号，确认：
- ✅ 连续两页不用相同布局
- ✅ 每3-4页有一个「呼吸页」（D/D2）
- ✅ 信息密集页(G/H/I)后面跟轻量页(D/D2/A)
- ✅ 深色/浅色交替，不连续3页同色调

### 布局与场景匹配

| 场景 | 优先使用 | 次要使用 |
|------|---------|---------|
| 数据报告 | G, H, I, B | A, D, K |
| 团队分享 | D, F, C, E | A, B, L |
| 述职汇报 | G, B, C, A | D, H, I, K |

---

## Layout A — 左右分栏 · 杂志排版

**适用**：概念解释、归因分析、图文搭配、核心观点阐述

**变体**：
- A1: 左文(60%) + 右视觉元素(40%)
- A2: 左视觉(40%) + 右文(60%)（镜像）
- A3: 左文(50%) + 右代码块/终端(50%)

```html
<!-- A1: 左文右视觉 -->
<div style="display:flex; width:90%; max-width:1100px; gap:48px;">
  <div style="flex:1.2; display:flex; flex-direction:column; justify-content:center;">
    <div class="anim-fade-left delay-1" style="font-size:.72rem; font-weight:700; color:var(--accent); letter-spacing:2px; text-transform:uppercase; margin-bottom:14px;">SECTION LABEL</div>
    <div class="anim-fade-left delay-2" style="font-family:'Playfair Display',serif; font-size:clamp(1.8rem,4vw,2.6rem); font-weight:900; color:var(--text-primary); margin-bottom:20px; line-height:1.2;">主标题<br>第二行</div>
    <div class="anim-fade-left delay-3" style="font-size:.92rem; color:var(--text-secondary); line-height:1.8; max-width:400px;">正文描述。可以有<span style="background:linear-gradient(transparent 60%, var(--accent-light) 60%); padding:0 2px;">高亮标记</span>强调关键词。</div>
  </div>
  <div style="flex:1; display:flex; align-items:center; justify-content:center;">
    <!-- 右侧：2x2网格 / 单张图片 / 代码块 / 图表 -->
  </div>
</div>
```

---

## Layout B — 大数字描边 · 步骤感

**适用**：流程步骤、方法论、技术架构、工作流

**变体**：
- B1: 描边空心数字（标准）
- B2: 实心大数字 + 小标签（紧凑版，适合4-5项）

```html
<!-- B1: 描边空心 -->
<div style="display:flex; flex-direction:column; max-width:750px; margin:0 auto;">
  <div class="anim-fade-up delay-N" style="display:flex; align-items:flex-start; gap:28px; padding:24px 0; border-bottom:1px solid rgba(0,0,0,.06);">
    <div style="font-family:'Playfair Display',serif; font-size:clamp(3.5rem,9vw,5.5rem); font-weight:900; color:transparent; -webkit-text-stroke:2px var(--accent); line-height:1; min-width:90px;">01</div>
    <div style="padding-top:8px; flex:1;">
      <div style="font-size:.7rem; font-weight:700; color:var(--accent); letter-spacing:2px; text-transform:uppercase; margin-bottom:6px;">CATEGORY</div>
      <div style="font-size:1.2rem; font-weight:900; color:var(--text-primary); margin-bottom:8px;">步骤标题</div>
      <div style="font-size:.88rem; color:var(--text-secondary); line-height:1.7;">描述文字，控制在2行以内...</div>
    </div>
  </div>
</div>

<!-- B2: 紧凑版（4-5项时用） -->
<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(200px, 1fr)); gap:20px; max-width:900px;">
  <div class="anim-scale delay-N" style="text-align:center; padding:24px 16px;">
    <div style="font-family:'Playfair Display',serif; font-size:2.5rem; font-weight:900; color:var(--accent); margin-bottom:8px;">01</div>
    <div style="font-size:.95rem; font-weight:700; color:var(--text-primary); margin-bottom:6px;">标题</div>
    <div style="font-size:.8rem; color:var(--text-secondary); line-height:1.5;">说明</div>
  </div>
</div>
```

---

## Layout C — 竖向时间轴 · 故事线

**适用**：项目里程碑、迭代历程、季度回顾、成长路径

```html
<div style="position:relative; padding-left:48px; max-width:650px; margin:0 auto;">
  <div style="position:absolute; left:14px; top:8px; bottom:8px; width:2.5px; background:linear-gradient(to bottom, var(--accent), var(--accent-light)); border-radius:2px;"></div>
  <!-- 节点 -->
  <div class="anim-fade-left delay-N" style="position:relative; margin-bottom:32px;">
    <div class="pulse-anim" style="position:absolute; left:-42px; top:6px; width:14px; height:14px; border-radius:50%; background:var(--accent); border:3px solid var(--bg-light);"></div>
    <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
      <span style="font-size:.72rem; font-family:'JetBrains Mono'; color:var(--accent); font-weight:600;">2024.Q3</span>
      <span style="font-size:1.05rem; font-weight:700; color:var(--text-primary);">节点标题</span>
    </div>
    <div style="font-size:.88rem; color:var(--text-secondary); line-height:1.7; background:#fff; padding:16px 20px; border-radius:12px; box-shadow:0 2px 8px rgba(0,0,0,.04);">
      节点描述内容...
    </div>
  </div>
</div>
```

---

## Layout D — 全屏大字 · 沉浸式（封面/金句/章节）

**适用**：封面、结尾、金句页、章节分隔、核心理念

**变体**：
- D1: 深色背景 + 渐变文字（封面/结尾）
- D2: 浅色背景 + 超大装饰文字（章节分隔）

```html
<!-- D1: 深色 -->
<div class="slide" data-dark="true" style="background:linear-gradient(180deg, var(--bg-dark-start), var(--bg-dark-end));">
  <div style="text-align:center; max-width:700px;">
    <div class="anim-scale delay-1 float-anim icon-wrap" style="margin-bottom:28px;"><!-- SVG 48-56px --></div>
    <div class="anim-fade-up delay-2" style="font-size:.75rem; color:var(--accent); font-weight:700; letter-spacing:3px; margin-bottom:20px;">LABEL</div>
    <div class="anim-fade-up delay-3" style="font-family:'Playfair Display',serif; font-size:clamp(2.4rem,5.5vw,4rem); font-weight:900; line-height:1.25; background:var(--title-gradient); -webkit-background-clip:text; -webkit-text-fill-color:transparent; margin-bottom:24px;">大标题文字</div>
    <div class="anim-fade-up delay-4" style="font-size:1rem; color:var(--text-dark-secondary); line-height:1.9;">副标题/正文描述</div>
    <div class="anim-fade-up delay-5" style="margin-top:40px; width:40px; height:2px; background:var(--accent); margin-left:auto; margin-right:auto;"></div>
  </div>
</div>

<!-- D2: 浅色章节分隔（带巨大背景装饰数字） -->
<div class="slide" data-dark="false" style="background:var(--bg-light-start); position:relative; overflow:hidden;">
  <!-- 背景装饰数字 -->
  <div style="position:absolute; right:-5%; top:50%; transform:translateY(-50%); font-family:'Playfair Display',serif; font-size:clamp(8rem,25vw,18rem); font-weight:900; color:var(--accent); opacity:.06;">02</div>
  <div style="position:relative; z-index:1; max-width:600px;">
    <div class="anim-fade-up delay-2" style="font-size:.72rem; font-weight:700; color:var(--accent); letter-spacing:2px; margin-bottom:16px;">PART TWO</div>
    <div class="anim-fade-up delay-3" style="font-size:clamp(2rem,5vw,3.2rem); font-weight:900; color:var(--text-primary); line-height:1.3;">章节标题<br>可以两行</div>
    <div class="anim-fade-up delay-4" style="margin-top:20px; font-size:.9rem; color:var(--text-secondary); line-height:1.7;">简短描述这部分要讲什么</div>
  </div>
</div>
```

---

## Layout E — 横向标签 · 分类展示

**适用**：多维度分析、分类功能、平级概念对比

```html
<div style="text-align:center; width:90%; max-width:850px;">
  <div class="anim-fade-up delay-2" style="display:flex; gap:10px; justify-content:center; margin-bottom:28px; flex-wrap:wrap;">
    <div style="background:var(--text-primary); color:#fff; padding:10px 22px; border-radius:24px; font-size:.82rem; font-weight:600; cursor:pointer;">当前选中</div>
    <div style="background:transparent; color:var(--text-primary); padding:10px 22px; border-radius:24px; font-size:.82rem; border:1.5px solid #e2e8f0; cursor:pointer;">其他项</div>
  </div>
  <div style="display:grid; grid-template-columns:1fr 1fr; gap:16px; text-align:left;">
    <!-- 用统一形态的卡片填充 -->
  </div>
</div>
```

---

## Layout F — 交错色块 · 蛇形布局

**适用**：功能亮点、成果展示、卖点列举

奇数行：左文右色块；偶数行：左色块右文

```html
<div style="display:flex; flex-direction:column; gap:16px; max-width:800px;">
  <!-- 奇数行 -->
  <div class="anim-fade-left delay-N" style="display:flex; gap:16px; min-height:100px;">
    <div style="flex:1.6; background:#fff; border-radius:14px; padding:22px 26px; box-shadow:0 4px 16px rgba(0,0,0,.04); display:flex; flex-direction:column; justify-content:center; transition:transform .3s;" onmouseover="this.style.transform='translateX(6px)'" onmouseout="this.style.transform='translateX(0)'">
      <div style="font-size:.68rem; color:var(--accent); font-weight:700; letter-spacing:1.5px; margin-bottom:5px;">LABEL</div>
      <div style="font-size:1.02rem; font-weight:700; color:var(--text-primary); margin-bottom:5px;">标题</div>
      <div style="font-size:.84rem; color:var(--text-secondary); line-height:1.5;">描述内容</div>
    </div>
    <div style="flex:.7; background:var(--bg-dark-start); border-radius:14px; display:flex; align-items:center; justify-content:center;">
      <div class="float-anim icon-wrap"><!-- SVG 36px --></div>
    </div>
  </div>
</div>
```

---

## Layout G — KPI 数据卡片

**适用**：核心指标展示、成果总览、季度数据、述职开篇

**变体**：
- G1: 3列等宽（标准）
- G2: 1大+2小（突出核心指标）
- G3: 横向长条卡（适合4-5个指标）

```html
<!-- G1: 3列标准 -->
<div style="display:grid; grid-template-columns:repeat(3,1fr); gap:20px; max-width:800px; margin:0 auto;">
  <div class="anim-scale delay-N" style="background:#fff; border-radius:16px; padding:32px 20px; text-align:center; box-shadow:0 6px 20px rgba(0,0,0,.05); border-top:3px solid var(--accent); transition:transform .3s;" onmouseover="this.style.transform='translateY(-6px)'" onmouseout="this.style.transform='translateY(0)'">
    <div class="icon-wrap" style="margin-bottom:12px;"><!-- SVG 24px --></div>
    <div style="font-family:'Playfair Display',serif; font-size:clamp(2rem,5vw,3rem); font-weight:900; color:var(--accent);">+42%</div>
    <div style="font-size:.85rem; font-weight:600; color:var(--text-primary); margin-top:8px;">指标名称</div>
    <div style="font-size:.72rem; color:var(--text-secondary); margin-top:4px;">vs 上季度</div>
  </div>
</div>

<!-- G2: 1大+2小 -->
<div style="display:grid; grid-template-columns:1.5fr 1fr 1fr; gap:20px; max-width:850px; margin:0 auto; align-items:stretch;">
  <!-- 大卡 -->
  <div class="anim-scale delay-2" style="background:var(--accent); border-radius:16px; padding:40px 28px; text-align:center; color:#fff; grid-row:span 1;">
    <div style="font-family:'Playfair Display',serif; font-size:3.5rem; font-weight:900;">128%</div>
    <div style="font-size:.9rem; font-weight:600; margin-top:10px;">核心目标达成率</div>
  </div>
  <!-- 小卡x2 -->
  <div class="anim-scale delay-3" style="background:#fff; border-radius:16px; padding:28px 20px; text-align:center; border-top:3px solid var(--accent); box-shadow:0 4px 16px rgba(0,0,0,.04);">
    <div style="font-family:'Playfair Display',serif; font-size:2rem; font-weight:900; color:var(--accent);">+23%</div>
    <div style="font-size:.8rem; color:var(--text-secondary); margin-top:8px;">转化率提升</div>
  </div>
  <div class="anim-scale delay-4" style="background:#fff; border-radius:16px; padding:28px 20px; text-align:center; border-top:3px solid var(--accent); box-shadow:0 4px 16px rgba(0,0,0,.04);">
    <div style="font-family:'Playfair Display',serif; font-size:2rem; font-weight:900; color:var(--accent);">-5.2%</div>
    <div style="font-size:.8rem; color:var(--text-secondary); margin-top:8px;">跳出率下降</div>
  </div>
</div>
```

---

## Layout H — 图表展示页

**适用**：趋势数据、对比分析、截图展示

**变体**：
- H1: 上图下洞察（标准）
- H2: 左图右结论（图+文字分析）
- H3: 全宽截图 + 标注

```html
<!-- H1: 上图下洞察 -->
<div style="max-width:750px; margin:0 auto;">
  <!-- 图表区（代码画 或 截图） -->
  <div class="anim-fade-up delay-2" style="background:#fff; border-radius:16px; padding:28px; box-shadow:0 4px 16px rgba(0,0,0,.04); margin-bottom:20px;">
    <!-- 柱状图/折线图/截图 -->
  </div>
  <!-- 洞察条 -->
  <div class="anim-fade-up delay-3" style="background:#fff; border-radius:12px; padding:14px 22px; border-left:4px solid var(--accent); box-shadow:0 2px 8px rgba(0,0,0,.03); font-size:.88rem; color:var(--text-primary); line-height:1.6;">
    <strong style="color:var(--accent);">洞察：</strong>结论描述...
  </div>
</div>

<!-- H2: 左图右结论 -->
<div style="display:flex; gap:32px; width:90%; max-width:1000px; align-items:center;">
  <div class="anim-fade-left delay-2" style="flex:1.3; background:#fff; border-radius:16px; padding:24px; box-shadow:0 4px 16px rgba(0,0,0,.04);">
    <!-- 图表/截图 -->
  </div>
  <div style="flex:1; display:flex; flex-direction:column; gap:16px;">
    <div class="anim-fade-right delay-3" style="font-size:1.1rem; font-weight:700; color:var(--text-primary);">关键发现</div>
    <div class="anim-fade-right delay-4" style="font-size:.88rem; color:var(--text-secondary); line-height:1.8;">分析文字...</div>
  </div>
</div>
```

---

## Layout I — 对比页（Before/After · 正/负）

**适用**：方案对比、前后变化、优劣分析

```html
<div style="display:flex; width:90%; max-width:950px; gap:24px;">
  <!-- Before / 问题 -->
  <div class="anim-fade-left delay-2" style="flex:1; display:flex; flex-direction:column;">
    <div style="font-size:.72rem; font-weight:700; color:#ef4444; letter-spacing:2px; margin-bottom:12px;">BEFORE</div>
    <div style="font-size:1.5rem; font-weight:900; color:var(--text-primary); margin-bottom:16px;">旧方案</div>
    <div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 4px 16px rgba(0,0,0,.04); flex:1;">
      <div style="font-size:.85rem; color:var(--text-secondary); line-height:2;">
        ✗ 问题1<br>✗ 问题2<br>✗ 问题3
      </div>
    </div>
  </div>
  <!-- 分割线 -->
  <div style="width:1px; background:linear-gradient(to bottom, transparent, var(--accent), transparent); margin:40px 0;"></div>
  <!-- After / 方案 -->
  <div class="anim-fade-right delay-3" style="flex:1; display:flex; flex-direction:column;">
    <div style="font-size:.72rem; font-weight:700; color:#10b981; letter-spacing:2px; margin-bottom:12px;">AFTER</div>
    <div style="font-size:1.5rem; font-weight:900; color:var(--text-primary); margin-bottom:16px;">新方案</div>
    <div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 4px 16px rgba(0,0,0,.04); flex:1;">
      <div style="font-size:.85rem; color:var(--text-secondary); line-height:2;">
        ✓ 改进1<br>✓ 改进2<br>✓ 改进3
      </div>
    </div>
  </div>
</div>
```

---

## Layout J — 引用/金句页（非深色版）

**适用**：用户评价、关键引用、核心定义

```html
<div style="max-width:650px; margin:0 auto; text-align:center;">
  <div class="anim-scale delay-2" style="background:#fff; border-radius:24px; padding:48px 40px; box-shadow:0 12px 40px rgba(0,0,0,.06); position:relative;">
    <div style="font-family:'Playfair Display',serif; font-size:4rem; color:var(--accent); opacity:.3; position:absolute; top:20px; left:32px; line-height:1;">"</div>
    <div style="font-family:'Playfair Display',serif; font-size:1.4rem; font-weight:700; font-style:italic; color:var(--text-primary); line-height:1.7; position:relative; z-index:1;">
      引用文字内容，可以是金句、用户评价或核心定义
    </div>
    <div style="margin-top:20px; font-size:.82rem; color:var(--text-secondary);">— 来源/作者</div>
  </div>
</div>
```

---

## Layout K — 表格/矩阵展示

**适用**：功能对比、数据表格、矩阵分析

```html
<div style="max-width:800px; margin:0 auto;">
  <div class="anim-fade-up delay-2" style="overflow:hidden; border-radius:16px; box-shadow:0 6px 24px rgba(0,0,0,.06);">
    <table style="width:100%; border-collapse:collapse; font-size:.82rem; background:#fff;">
      <thead>
        <tr style="background:var(--bg-dark-start); color:#fff;">
          <th style="padding:14px 20px; text-align:left; font-weight:600;">列标题</th>
          <th style="padding:14px 20px; text-align:left; font-weight:600;">列标题</th>
          <th style="padding:14px 20px; text-align:left; font-weight:600;">列标题</th>
        </tr>
      </thead>
      <tbody>
        <tr style="border-bottom:1px solid #f1f5f9;">
          <td style="padding:13px 20px; font-weight:600; color:var(--text-primary);">行标题</td>
          <td style="padding:13px 20px; color:var(--text-secondary);">内容</td>
          <td style="padding:13px 20px;"><span style="color:#10b981; font-weight:600;">✓</span></td>
        </tr>
        <tr style="border-bottom:1px solid #f1f5f9; background:#f8fafc;">
          <td style="padding:13px 20px; font-weight:600; color:var(--text-primary);">行标题</td>
          <td style="padding:13px 20px; color:var(--text-secondary);">内容</td>
          <td style="padding:13px 20px;"><span style="color:#ef4444; font-weight:600;">✗</span></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
```

---

## Layout L — 多列列表/要点卡（信息密集）

**适用**：功能清单、禁忌列表、规则说明

```html
<div style="display:grid; grid-template-columns:1fr 1fr; gap:20px; max-width:850px; margin:0 auto;">
  <div class="anim-fade-up delay-2" style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 4px 12px rgba(0,0,0,.04);">
    <div style="display:flex; align-items:center; gap:10px; margin-bottom:14px;">
      <div style="width:28px; height:28px; border-radius:8px; background:var(--accent-bg); display:flex; align-items:center; justify-content:center;">
        <span class="icon-wrap"><!-- SVG 16px --></span>
      </div>
      <div style="font-size:.92rem; font-weight:700; color:var(--text-primary);">区块标题</div>
    </div>
    <div style="font-size:.82rem; color:var(--text-secondary); line-height:1.8;">
      • 要点一<br>• 要点二<br>• 要点三
    </div>
  </div>
</div>
```


---

## Layout M — 数据大字报 · 纯文字冲击

**适用**：核心KPI展示、数据洞察、单一结论强调

**特点**：没有卡片，数字本身就是视觉主体。靠字号极端对比+留白创造冲击力。

```html
<!-- M1: 单指标全屏 -->
<div style="max-width:800px; text-align:left; padding:0 60px;">
  <div class="anim-fade-up delay-1" style="font-size:.72rem; font-weight:700; color:var(--accent); letter-spacing:2px; text-transform:uppercase; margin-bottom:16px;">SECTION LABEL</div>
  <div class="anim-fade-up delay-2" style="font-family:'Playfair Display',serif; font-size:clamp(4rem,12vw,8rem); font-weight:900; color:var(--text-primary); line-height:1; margin-bottom:16px;">189.8<span style="font-size:.3em; color:var(--text-secondary); font-weight:400;">亿</span></div>
  <div class="anim-fade-up delay-3" style="font-size:1.1rem; color:var(--text-secondary); line-height:1.7; max-width:500px;">
    2025年全球AI漫剧市场规模，同比增长276%。<br>
    这个数字是年初行业预测值的两倍。
  </div>
  <div class="anim-fade-up delay-4" style="margin-top:24px; display:flex; gap:32px;">
    <div>
      <span style="font-family:'JetBrains Mono'; font-size:.72rem; color:var(--positive); font-weight:600;">▲ 276%</span>
      <span style="font-size:.72rem; color:var(--text-secondary); margin-left:6px;">同比</span>
    </div>
    <div>
      <span style="font-family:'JetBrains Mono'; font-size:.72rem; color:var(--accent); font-weight:600;">6万+</span>
      <span style="font-size:.72rem; color:var(--text-secondary); margin-left:6px;">上线剧目</span>
    </div>
  </div>
</div>

<!-- M2: 双指标并列（无卡片，靠分割线区分） -->
<div style="display:flex; width:90%; max-width:1000px; gap:0;">
  <div class="anim-fade-left delay-2" style="flex:1; padding:0 40px; border-right:1px solid var(--divider);">
    <div style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; margin-bottom:12px;">DOMESTIC</div>
    <div style="font-family:'Playfair Display',serif; font-size:clamp(2.5rem,7vw,4.5rem); font-weight:900; color:var(--text-primary); line-height:1;">168<span style="font-size:.35em; color:var(--text-secondary);">亿</span></div>
    <div style="font-size:.85rem; color:var(--text-secondary); margin-top:12px; line-height:1.6;">中国市场占全球九成<br>用户规模突破2.2亿</div>
  </div>
  <div class="anim-fade-right delay-3" style="flex:1; padding:0 40px;">
    <div style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; margin-bottom:12px;">OVERSEAS</div>
    <div style="font-family:'Playfair Display',serif; font-size:clamp(2.5rem,7vw,4.5rem); font-weight:900; color:var(--text-primary); line-height:1;">~1<span style="font-size:.35em; color:var(--text-secondary);">亿$</span></div>
    <div style="font-size:.85rem; color:var(--text-secondary); margin-top:12px; line-height:1.6;">活跃用户1.5亿<br>2026年预计增长550%</div>
  </div>
</div>
```

---

## Layout N — 条目列表 · 分割线节奏

**适用**：工具列表、平台枚举、规则说明、多项并列信息

**特点**：不用卡片包裹，用分割线+左对齐文字创造节奏。像杂志目录或报纸排版。

```html
<div style="max-width:750px; margin:0 auto;">
  <div class="anim-fade-up delay-N" style="display:flex; align-items:baseline; gap:20px; padding:20px 0; border-bottom:1px solid var(--divider);">
    <div style="font-family:'JetBrains Mono'; font-size:.7rem; color:var(--accent); font-weight:600; min-width:60px;">01</div>
    <div style="flex:1;">
      <div style="font-size:1rem; font-weight:700; color:var(--text-primary); margin-bottom:4px;">条目标题</div>
      <div style="font-size:.82rem; color:var(--text-secondary); line-height:1.6;">条目描述，不超过两行。关键信息用<span style="color:var(--accent); font-weight:600;">强调色</span>标出。</div>
    </div>
    <div style="font-size:.75rem; color:var(--text-secondary); text-align:right; min-width:80px;">补充标注</div>
  </div>
  <!-- 重复多条 -->
</div>
```

---

## Layout O — 色块分区 · 无卡片对比

**适用**：两个概念对比、正反论证、双方案展示

**特点**：整页分成两个背景色块，不用卡片，靠背景色本身区分左右内容。

```html
<div style="display:flex; width:100%; height:100%;">
  <!-- 左区块：深色背景 -->
  <div style="flex:1; background:var(--bg-dark-start); padding:60px 48px; display:flex; flex-direction:column; justify-content:center; color:#fff;">
    <div class="anim-fade-left delay-1" style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; margin-bottom:12px;">LEFT LABEL</div>
    <div class="anim-fade-left delay-2" style="font-size:1.6rem; font-weight:900; margin-bottom:16px;">左侧标题</div>
    <div class="anim-fade-left delay-3" style="font-size:.85rem; color:var(--text-dark-secondary); line-height:1.8;">
      左侧描述内容，可以多行。<br>不需要卡片容器，背景色就是分区。
    </div>
  </div>
  <!-- 右区块：浅色背景 -->
  <div style="flex:1; background:var(--bg-light-start); padding:60px 48px; display:flex; flex-direction:column; justify-content:center;">
    <div class="anim-fade-right delay-1" style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; margin-bottom:12px;">RIGHT LABEL</div>
    <div class="anim-fade-right delay-2" style="font-size:1.6rem; font-weight:900; color:var(--text-primary); margin-bottom:16px;">右侧标题</div>
    <div class="anim-fade-right delay-3" style="font-size:.85rem; color:var(--text-secondary); line-height:1.8;">
      右侧描述内容，可以多行。<br>和左侧形成视觉对比。
    </div>
  </div>
</div>
```

---

## Layout P — 混合密度 · 大留白+密集区

**适用**：一个核心观点+多个支撑细节、结论+证据

**特点**：页面上半部分大量留白只放一句话，下半部分密集排列支撑信息。打破均匀分布。

```html
<div style="width:90%; max-width:1000px; display:flex; flex-direction:column; height:70vh; justify-content:space-between;">
  <!-- 上部：大留白，只有一句核心观点 -->
  <div class="anim-fade-up delay-1" style="padding-top:20px;">
    <div style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; margin-bottom:12px;">CORE INSIGHT</div>
    <div style="font-size:clamp(1.6rem,4vw,2.4rem); font-weight:900; color:var(--text-primary); line-height:1.4; max-width:600px;">
      核心观点只用一句话，<br>大量留白让它呼吸。
    </div>
  </div>
  <!-- 下部：密集支撑信息 -->
  <div class="anim-fade-up delay-3" style="display:flex; gap:32px; padding-bottom:20px; border-top:1px solid var(--divider); padding-top:24px;">
    <div style="flex:1;">
      <div style="font-size:.68rem; color:var(--accent); font-weight:600; margin-bottom:6px;">证据 1</div>
      <div style="font-size:.8rem; color:var(--text-secondary); line-height:1.6;">支撑细节描述...</div>
    </div>
    <div style="flex:1;">
      <div style="font-size:.68rem; color:var(--accent); font-weight:600; margin-bottom:6px;">证据 2</div>
      <div style="font-size:.8rem; color:var(--text-secondary); line-height:1.6;">支撑细节描述...</div>
    </div>
    <div style="flex:1;">
      <div style="font-size:.68rem; color:var(--accent); font-weight:600; margin-bottom:6px;">证据 3</div>
      <div style="font-size:.8rem; color:var(--text-secondary); line-height:1.6;">支撑细节描述...</div>
    </div>
  </div>
</div>
```

---

## 布局选择更新总表

| 布局 | 是否用卡片 | 视觉特征 | 适合场景 |
|------|-----------|---------|---------|
| A | 可选 | 左右分栏 | 概念解释 |
| B | 否 | 大数字+分割线 | 步骤流程 |
| C | 可选 | 竖线+节点 | 时间轴 |
| D | 否 | 纯文字+大留白 | 封面/金句 |
| E | 是 | 标签+网格 | 分类展示 |
| F | 混合 | 文字+色块交错 | 功能亮点 |
| G | 是 | KPI数据卡 | 数据总览 |
| H | 可选 | 图表+洞察 | 趋势分析 |
| I | 可选 | 左右对比 | Before/After |
| J | 是(单个) | 引用卡 | 金句/评价 |
| K | 否 | 表格 | 矩阵对比 |
| L | 是 | 2列卡片 | 信息密集 |
| **M** | **否** | **数字冲击+留白** | **核心KPI** |
| **N** | **否** | **分割线+条目** | **列表枚举** |
| **O** | **否** | **色块背景分区** | **概念对比** |
| **P** | **否** | **上留白+下密集** | **观点+证据** |

**使用原则更新**：
- 一份PPT中，无卡片布局(B/D/M/N/O/P)应占至少 **40%**
- 有卡片布局(E/G/L)不超过 **30%**
- 混合布局(A/C/F/H/I)占剩余 **30%**


---

## Layout Q — 咨询密集页 · 标题+要点+数据

**适用**：数据分析报告的核心内容页。一页同时承载标题、多个要点、关键数据和结论。

**特点**：信息密度高但有视觉层次。顶部标题区(10%) + 中部内容区(70%) + 底部洞察区(20%)。不用卡片包裹，用分割线/缩进/字号对比区分层级。

**变体**：
- Q1: 标题 + 2列要点 + 底部洞察（最常用）
- Q2: 标题 + 左文右数据 + 底部结论（图文结合）
- Q3: 标题 + 表格 + 底部洞察（保留原文表格）

```html
<!-- Q1: 标题 + 2列要点 + 底部洞察 -->
<div style="width:90%; max-width:1050px; display:flex; flex-direction:column; gap:0;">
  <!-- 顶部标题区 -->
  <div class="anim-fade-up delay-1" style="margin-bottom:24px;">
    <div style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; text-transform:uppercase; margin-bottom:8px;">SECTION LABEL</div>
    <div style="font-size:clamp(1.4rem,3vw,2rem); font-weight:900; color:var(--text-primary); margin-bottom:6px;">页面标题（结论先行）</div>
    <div style="font-size:.82rem; color:var(--text-secondary); line-height:1.6;">一句话摘要描述，概括本页核心发现</div>
  </div>
  <!-- 中部内容区：2列要点 -->
  <div class="anim-fade-up delay-2" style="display:grid; grid-template-columns:1fr 1fr; gap:24px 40px; padding:20px 0; border-top:1px solid var(--divider); border-bottom:1px solid var(--divider);">
    <div>
      <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
        <div style="width:4px; height:16px; background:var(--accent); border-radius:2px;"></div>
        <span style="font-size:.88rem; font-weight:700; color:var(--text-primary);">要点标题一</span>
      </div>
      <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.7; padding-left:12px;">
        要点描述文字，可以2-3行。保留原文的严谨表述，关键数据用<span style="color:var(--accent); font-weight:600;">强调色</span>标出。
      </p>
    </div>
    <div>
      <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
        <div style="width:4px; height:16px; background:var(--accent); border-radius:2px;"></div>
        <span style="font-size:.88rem; font-weight:700; color:var(--text-primary);">要点标题二</span>
      </div>
      <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.7; padding-left:12px;">
        要点描述文字，保持信息密度但用视觉层次区分主次。
      </p>
    </div>
    <div>
      <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
        <div style="width:4px; height:16px; background:var(--accent); border-radius:2px;"></div>
        <span style="font-size:.88rem; font-weight:700; color:var(--text-primary);">要点标题三</span>
      </div>
      <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.7; padding-left:12px;">
        更多内容...来源可在末尾小字标注。
      </p>
    </div>
    <div>
      <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
        <div style="width:4px; height:16px; background:var(--accent); border-radius:2px;"></div>
        <span style="font-size:.88rem; font-weight:700; color:var(--text-primary);">要点标题四</span>
      </div>
      <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.7; padding-left:12px;">
        数据支撑描述...
      </p>
    </div>
  </div>
  <!-- 底部洞察区 -->
  <div class="anim-fade-up delay-3" style="padding-top:16px; display:flex; align-items:flex-start; gap:12px;">
    <div style="width:3px; height:100%; min-height:32px; background:var(--accent); border-radius:2px; flex-shrink:0;"></div>
    <div>
      <span style="font-size:.75rem; font-weight:700; color:var(--accent);">核心洞察</span>
      <p style="font-size:.8rem; color:var(--text-primary); line-height:1.6; margin-top:4px;">结论性总结，一句话说清楚 so what 和 next step。</p>
    </div>
  </div>
</div>

<!-- Q2: 标题 + 左文右数据 -->
<div style="width:90%; max-width:1050px;">
  <!-- 标题区 -->
  <div class="anim-fade-up delay-1" style="margin-bottom:20px;">
    <div style="font-size:.68rem; font-weight:600; color:var(--accent); letter-spacing:2px; margin-bottom:8px;">LABEL</div>
    <div style="font-size:clamp(1.4rem,3vw,2rem); font-weight:900; color:var(--text-primary);">页面标题</div>
  </div>
  <!-- 双栏内容 -->
  <div class="anim-fade-up delay-2" style="display:grid; grid-template-columns:1.3fr 1fr; gap:36px; padding:20px 0; border-top:1px solid var(--divider);">
    <!-- 左：正文要点 -->
    <div style="display:flex; flex-direction:column; gap:14px;">
      <p style="font-size:.82rem; color:var(--text-secondary); line-height:1.8;">
        • 第一个核心观点，保留原文完整表述<br>
        • 第二个观点，关键数据<span style="font-family:'JetBrains Mono'; color:var(--accent); font-weight:600;">+276%</span>标出<br>
        • 第三个观点，来源信息可在此标注
      </p>
      <p style="font-size:.72rem; color:var(--text-secondary); font-style:italic;">来源：DataEye Research 2025</p>
    </div>
    <!-- 右：关键数据面板 -->
    <div style="display:flex; flex-direction:column; gap:12px;">
      <div style="padding:14px 18px; border-left:3px solid var(--accent); background:var(--accent-bg);">
        <div style="font-family:'Playfair Display',serif; font-size:1.8rem; font-weight:900; color:var(--text-primary);">189.8<span style="font-size:.8rem; color:var(--text-secondary);">亿</span></div>
        <div style="font-size:.72rem; color:var(--text-secondary);">2025全球市场规模</div>
      </div>
      <div style="padding:14px 18px; border-left:3px solid var(--positive); background:rgba(16,185,129,.05);">
        <div style="font-family:'Playfair Display',serif; font-size:1.8rem; font-weight:900; color:var(--positive);">276%</div>
        <div style="font-size:.72rem; color:var(--text-secondary);">同比增长</div>
      </div>
    </div>
  </div>
  <!-- 底部洞察 -->
  <div class="anim-fade-up delay-3" style="padding-top:16px; background:var(--accent-bg); padding:12px 16px; margin-top:12px; border-left:3px solid var(--accent);">
    <p style="font-size:.78rem; color:var(--text-primary); line-height:1.5;"><strong style="color:var(--accent);">So What：</strong>结论和行动建议</p>
  </div>
</div>
```

---

## 布局总结更新

| 布局 | 信息密度 | 适合场景 |
|------|---------|---------|
| A-F | 中 | 通用 |
| G-L | 中-高 | 数据展示 |
| M | 低（大字冲击） | KPI强调 |
| N | 中 | 列表枚举 |
| O | 中 | 概念对比 |
| P | 低+高混合 | 观点+证据 |
| **Q** | **高** | **数据报告核心内容页** |
