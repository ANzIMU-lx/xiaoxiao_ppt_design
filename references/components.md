# 组件库 v2

> 可直接复制使用的代码片段。所有组件禁止使用 HTML 默认样式。

---

## 数据类组件

### 1. KPI 单卡（带趋势）

```html
<div style="background:#fff; border-radius:16px; padding:28px 24px; text-align:center; border-top:3px solid var(--accent); box-shadow:0 4px 16px rgba(0,0,0,.04); transition:transform .3s;" onmouseover="this.style.transform='translateY(-4px)'" onmouseout="this.style.transform='translateY(0)'">
  <div style="font-family:'JetBrains Mono'; font-size:.7rem; color:#10b981; font-weight:600; margin-bottom:6px;">▲ 12.5% MoM</div>
  <div style="font-family:'Playfair Display',serif; font-size:clamp(2rem,5vw,3rem); font-weight:900; color:var(--accent);">2.4M</div>
  <div style="font-size:.82rem; font-weight:600; color:var(--text-primary); margin-top:8px;">月活跃用户</div>
</div>
```

### 2. 数据对比卡（正/负双向）

```html
<div style="display:flex; gap:16px;">
  <div style="flex:1; background:#fff; border-radius:14px; padding:24px; text-align:center; border-top:3px solid #10b981; box-shadow:0 4px 12px rgba(0,0,0,.03);">
    <div style="font-family:'Playfair Display',serif; font-size:2.2rem; font-weight:900; color:#10b981;">↑ 23%</div>
    <div style="font-size:.82rem; color:var(--text-secondary); margin-top:8px;">转化率提升</div>
  </div>
  <div style="flex:1; background:#fff; border-radius:14px; padding:24px; text-align:center; border-top:3px solid #ef4444; box-shadow:0 4px 12px rgba(0,0,0,.03);">
    <div style="font-family:'Playfair Display',serif; font-size:2.2rem; font-weight:900; color:#ef4444;">↓ 5%</div>
    <div style="font-size:.82rem; color:var(--text-secondary); margin-top:8px;">跳出率降低</div>
  </div>
</div>
```

### 3. 洞察条（数据结论，必须跟在图表后面）

```html
<div style="background:#fff; border-radius:12px; padding:14px 22px; border-left:4px solid var(--accent); box-shadow:0 2px 8px rgba(0,0,0,.03); font-size:.88rem; color:var(--text-primary); line-height:1.6;">
  <strong style="color:var(--accent);">洞察：</strong>数据结论描述，一句话说清楚 so what...
</div>
```

### 4. 简易柱状图

```html
<div style="display:flex; align-items:flex-end; justify-content:center; gap:20px; height:180px; padding:0 20px;">
  <div style="display:flex; flex-direction:column; align-items:center; gap:6px;">
    <div style="font-family:'JetBrains Mono'; font-size:.7rem; font-weight:600; color:var(--text-primary);">88%</div>
    <div style="width:44px; height:158px; background:var(--accent); border-radius:6px 6px 0 0;"></div>
    <div style="font-size:.7rem; color:var(--text-secondary);">Q1</div>
  </div>
  <div style="display:flex; flex-direction:column; align-items:center; gap:6px;">
    <div style="font-family:'JetBrains Mono'; font-size:.7rem; font-weight:600; color:var(--text-primary);">72%</div>
    <div style="width:44px; height:130px; background:var(--accent); border-radius:6px 6px 0 0; opacity:.65;"></div>
    <div style="font-size:.7rem; color:var(--text-secondary);">Q2</div>
  </div>
  <!-- 更多柱... -->
</div>
```

### 5. 进度环

```html
<div style="text-align:center;">
  <svg width="90" height="90" viewBox="0 0 90 90">
    <circle cx="45" cy="45" r="38" fill="none" stroke="#e2e8f0" stroke-width="6"/>
    <circle cx="45" cy="45" r="38" fill="none" stroke="var(--accent)" stroke-width="6" stroke-dasharray="239" stroke-dashoffset="48" stroke-linecap="round" transform="rotate(-90 45 45)"/>
  </svg>
  <div style="font-family:'Playfair Display',serif; font-size:1.4rem; font-weight:900; color:var(--text-primary); margin-top:8px;">80%</div>
  <div style="font-size:.72rem; color:var(--text-secondary);">完成度</div>
</div>
```

---

## 流程/结构类组件

### 6. 横向流程图

```html
<div style="display:flex; align-items:center; justify-content:center; gap:0; flex-wrap:wrap;">
  <div style="background:var(--accent); color:#fff; padding:12px 20px; border-radius:10px; font-size:.8rem; font-weight:600; text-align:center;">步骤1</div>
  <svg width="32" height="24" viewBox="0 0 24 24" stroke="var(--accent)" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
  <div style="background:var(--accent); color:#fff; padding:12px 20px; border-radius:10px; font-size:.8rem; font-weight:600; text-align:center;">步骤2</div>
  <svg width="32" height="24" viewBox="0 0 24 24" stroke="var(--accent)" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
  <div style="background:var(--accent); color:#fff; padding:12px 20px; border-radius:10px; font-size:.8rem; font-weight:600; text-align:center;">步骤3</div>
</div>
```

### 7. 漏斗图（竖向）

```html
<div style="display:flex; flex-direction:column; align-items:center; gap:4px; max-width:400px; margin:0 auto;">
  <div style="background:var(--accent); color:#fff; padding:14px 0; border-radius:8px; width:100%; text-align:center; font-size:.82rem; font-weight:600;">访问 100,000</div>
  <div style="background:var(--accent); color:#fff; padding:14px 0; border-radius:8px; width:80%; text-align:center; font-size:.82rem; font-weight:600; opacity:.8;">注册 42,000</div>
  <div style="background:var(--accent); color:#fff; padding:14px 0; border-radius:8px; width:55%; text-align:center; font-size:.82rem; font-weight:600; opacity:.6;">激活 18,000</div>
  <div style="background:var(--accent); color:#fff; padding:14px 0; border-radius:8px; width:35%; text-align:center; font-size:.82rem; font-weight:600; opacity:.45;">付费 6,200</div>
</div>
```

---

## 展示类组件

### 8. 截图容器（带阴影）

```html
<div style="background:#fff; border-radius:16px; padding:16px; box-shadow:0 8px 32px rgba(0,0,0,.08); max-width:700px; margin:0 auto;">
  <img src="images/screenshot.png" style="width:100%; border-radius:8px; display:block;" alt="描述">
  <div style="margin-top:10px; font-size:.75rem; color:var(--text-secondary); text-align:center;">图片说明文字</div>
</div>
```

### 9. 代码块（终端风格）

```html
<div style="background:#0f172a; border-radius:12px; padding:24px 28px; font-family:'JetBrains Mono',monospace; font-size:.78rem; line-height:1.9; color:#e2e8f0; box-shadow:0 8px 24px rgba(0,0,0,.12); position:relative; overflow:hidden;">
  <div style="position:absolute; top:12px; left:16px; display:flex; gap:6px;">
    <div style="width:10px; height:10px; border-radius:50%; background:#ef4444;"></div>
    <div style="width:10px; height:10px; border-radius:50%; background:#f59e0b;"></div>
    <div style="width:10px; height:10px; border-radius:50%; background:#10b981;"></div>
  </div>
  <div style="margin-top:20px;">
    <span style="color:#94a3b8;">$</span> <span style="color:#60a5fa;">命令内容</span><br>
    <span style="color:#a5f3fc;">输出结果</span>
  </div>
</div>
```

### 10. 底部高亮栏（3列总结）

```html
<div style="display:flex; background:#fff; border-radius:16px; box-shadow:0 4px 20px rgba(0,0,0,.06); overflow:hidden; max-width:850px; margin:0 auto;">
  <div style="flex:1; padding:22px 24px; display:flex; align-items:center; gap:12px; border-right:1px solid #f1f5f9;">
    <div class="icon-wrap" style="width:36px; height:36px; border-radius:50%; background:var(--accent-bg); flex-shrink:0;"><!-- SVG 18px --></div>
    <div style="font-size:.82rem; color:var(--text-secondary); line-height:1.4;"><strong style="color:var(--text-primary);">关键词</strong>，说明</div>
  </div>
  <!-- 重复3项 -->
</div>
```

---

## 装饰/标记类组件

### 11. 标签/Badge

```html
<!-- 实心标签 -->
<span style="display:inline-block; background:var(--accent); color:#fff; padding:4px 12px; border-radius:4px; font-size:.7rem; font-weight:600;">标签</span>

<!-- 描边标签 -->
<span style="display:inline-block; border:1.5px solid var(--accent); color:var(--accent); padding:4px 12px; border-radius:4px; font-size:.7rem; font-weight:600;">标签</span>

<!-- 状态标签 -->
<span style="display:inline-block; background:#dcfce7; color:#166534; padding:4px 10px; border-radius:12px; font-size:.68rem; font-weight:600;">已完成</span>
<span style="display:inline-block; background:#fef3c7; color:#92400e; padding:4px 10px; border-radius:12px; font-size:.68rem; font-weight:600;">进行中</span>
```

### 12. 分割装饰线

```html
<!-- 短金线（用于深色页面底部） -->
<div style="width:40px; height:2px; background:var(--accent); border-radius:1px; margin:32px auto 0;"></div>

<!-- 渐变分割（用于浅色页面区块间） -->
<div style="width:100%; max-width:200px; height:1px; background:linear-gradient(to right, transparent, var(--accent), transparent); margin:32px auto;"></div>
```

### 13. 背景装饰数字

```html
<!-- 放在 slide 内部作为背景装饰 -->
<div style="position:absolute; right:-3%; top:50%; transform:translateY(-50%); font-family:'Playfair Display',serif; font-size:clamp(7rem,22vw,16rem); font-weight:900; color:var(--accent); opacity:.05; pointer-events:none;">03</div>
```

### 14. 高亮标记文字

```html
<!-- 在正文中使用 -->
<span style="background:linear-gradient(transparent 60%, var(--accent-light) 60%); padding:0 3px;">高亮关键词</span>
```


---

## 纯文字排版类组件（无卡片）

### 15. 数据大字（独立使用，不需容器）

```html
<!-- 单独一组KPI，靠字号对比和留白产生冲击 -->
<div>
  <div style="font-family:'Playfair Display',serif; font-size:clamp(3.5rem,10vw,7rem); font-weight:900; color:var(--text-primary); line-height:1;">
    276<span style="font-size:.3em; color:var(--text-secondary); font-weight:400;">%</span>
  </div>
  <div style="font-size:.85rem; color:var(--text-secondary); margin-top:8px;">同比增长 · 2024→2025</div>
</div>
```

### 16. 分割线条目（列表式，不用ul/卡片）

```html
<div style="display:flex; align-items:baseline; gap:20px; padding:18px 0; border-bottom:1px solid var(--divider);">
  <span style="font-family:'JetBrains Mono'; font-size:.7rem; color:var(--accent); font-weight:600; min-width:32px;">01</span>
  <div style="flex:1;">
    <span style="font-size:.92rem; font-weight:700; color:var(--text-primary);">条目标题</span>
    <span style="font-size:.78rem; color:var(--text-secondary); margin-left:12px;">补充说明文字</span>
  </div>
  <span style="font-family:'JetBrains Mono'; font-size:.72rem; color:var(--accent);">数据标注</span>
</div>
```

### 17. 文字强调块（背景色区分，非卡片）

```html
<!-- 用背景色做区分，不加圆角不加阴影 -->
<div style="background:var(--accent-bg); padding:24px 32px; margin:0 -32px;">
  <div style="font-size:.72rem; color:var(--accent); font-weight:700; letter-spacing:1px; margin-bottom:8px;">KEY POINT</div>
  <div style="font-size:1.05rem; font-weight:700; color:var(--text-primary); line-height:1.6;">
    关键结论或重要观点，用背景色块而非卡片来突出。<br>
    这种方式更像杂志排版，不像UI组件。
  </div>
</div>
```

### 18. 引用文字（纯文字，不用引用卡）

```html
<!-- 大引号+斜体，不需要卡片容器 -->
<div style="position:relative; padding-left:32px; max-width:600px;">
  <div style="position:absolute; left:0; top:-4px; font-family:'Playfair Display',serif; font-size:3rem; color:var(--accent); opacity:.4; line-height:1;">"</div>
  <div style="font-family:'Playfair Display',serif; font-size:1.2rem; font-weight:700; font-style:italic; color:var(--text-primary); line-height:1.7;">
    引用内容，不需要卡片包裹。靠引号和斜体字体来标识这是引用。
  </div>
  <div style="font-size:.75rem; color:var(--text-secondary); margin-top:12px;">— 来源</div>
</div>
```

### 19. 指标行（横向排列，用竖线分隔）

```html
<!-- 多个指标横向排列，竖线分隔，不用卡片 -->
<div style="display:flex; gap:0; align-items:center;">
  <div style="padding:0 28px;">
    <div style="font-family:'Playfair Display',serif; font-size:1.8rem; font-weight:900; color:var(--accent);">6万+</div>
    <div style="font-size:.7rem; color:var(--text-secondary); margin-top:4px;">上线剧目</div>
  </div>
  <div style="width:1px; height:40px; background:var(--divider);"></div>
  <div style="padding:0 28px;">
    <div style="font-family:'Playfair Display',serif; font-size:1.8rem; font-weight:900; color:var(--accent);">80%</div>
    <div style="font-size:.7rem; color:var(--text-secondary); margin-top:4px;">中国产能占比</div>
  </div>
  <div style="width:1px; height:40px; background:var(--divider);"></div>
  <div style="padding:0 28px;">
    <div style="font-family:'Playfair Display',serif; font-size:1.8rem; font-weight:900; color:var(--accent);">1.5亿</div>
    <div style="font-size:.7rem; color:var(--text-secondary); margin-top:4px;">海外活跃用户</div>
  </div>
</div>
```

### 20. 左侧竖色条标记（替代border-left卡片）

```html
<!-- 用粗色条做视觉锚点，不是卡片的border -->
<div style="display:flex; gap:16px; align-items:stretch;">
  <div style="width:4px; border-radius:2px; background:var(--accent); flex-shrink:0;"></div>
  <div>
    <div style="font-size:1rem; font-weight:700; color:var(--text-primary); margin-bottom:6px;">标题内容</div>
    <div style="font-size:.82rem; color:var(--text-secondary); line-height:1.7;">
      描述文字，不需要卡片背景和阴影。<br>
      竖色条本身就足够做视觉标识。
    </div>
  </div>
</div>
```


---

## 结构/导航类组件

### 21. 页面 Section Label（每页必有）

```html
<div style="font-size:.72rem; font-weight:700; color:var(--accent); letter-spacing:2px; text-transform:uppercase; margin-bottom:14px;">SECTION LABEL</div>
```

### 22. 页码（左上角）

```html
<span style="position:absolute; top:32px; left:40px; font-family:'Playfair Display',serif; font-size:1.1rem; font-weight:900; color:rgba(0,0,0,.35); z-index:50;">01</span>
<!-- 深色页用 color:rgba(255,255,255,.4) -->
```

### 23. 短装饰线（章节结尾/封面底部）

```html
<div style="width:40px; height:2px; background:var(--accent); border-radius:1px; margin-top:40px;"></div>
```

### 24. 渐变分割线（区块间）

```html
<div style="width:100%; max-width:200px; height:1px; background:linear-gradient(to right, transparent, var(--divider), transparent); margin:32px 0;"></div>
```

---

## 文字效果类组件

### 25. 高亮标记文字

```html
<span style="background:linear-gradient(transparent 60%, var(--accent-light) 60%); padding:0 3px;">关键词</span>
```

### 26. 描边空心大数字（装饰性）

```html
<div style="font-family:'Playfair Display',serif; font-size:clamp(3.5rem,9vw,5.5rem); font-weight:900; color:transparent; -webkit-text-stroke:2px var(--accent); line-height:1;">01</div>
```

### 27. 渐变文字（深色页标题）

```html
<div style="font-family:'Playfair Display',serif; font-size:clamp(2rem,5vw,3.5rem); font-weight:900; background:var(--title-gradient); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text; line-height:1.25;">标题文字</div>
```

### 28. 背景装饰大数字（半透明，position:absolute）

```html
<div style="position:absolute; right:-3%; top:50%; transform:translateY(-50%); font-family:'Playfair Display',serif; font-size:clamp(7rem,22vw,16rem); font-weight:900; color:var(--accent); opacity:.05; pointer-events:none;">02</div>
```

---

## 数据展示补充

### 29. 横向进度条

```html
<div style="margin-bottom:14px;">
  <div style="display:flex; justify-content:space-between; margin-bottom:6px;">
    <span style="font-size:.78rem; font-weight:600; color:var(--text-primary);">指标名称</span>
    <span style="font-family:'JetBrains Mono'; font-size:.72rem; color:var(--accent); font-weight:600;">78%</span>
  </div>
  <div style="height:6px; background:var(--divider); border-radius:3px; overflow:hidden;">
    <div style="height:100%; width:78%; background:var(--accent); border-radius:3px;"></div>
  </div>
</div>
```

### 30. 对比数据行（正负并列，不用卡片）

```html
<div style="display:flex; align-items:center; gap:16px; padding:14px 0; border-bottom:1px solid var(--divider);">
  <span style="font-size:.82rem; font-weight:600; color:var(--text-primary); min-width:100px;">指标名称</span>
  <div style="flex:1; display:flex; align-items:center; gap:8px;">
    <div style="height:4px; flex:1; background:var(--divider); border-radius:2px; overflow:hidden;">
      <div style="height:100%; width:72%; background:var(--positive); border-radius:2px;"></div>
    </div>
    <span style="font-family:'JetBrains Mono'; font-size:.72rem; color:var(--positive); font-weight:600; min-width:40px;">+72%</span>
  </div>
</div>
```

### 31. 迷你指标组（横向，适合底部总结）

```html
<div style="display:flex; gap:24px; padding-top:20px; border-top:1px solid var(--divider);">
  <div>
    <div style="font-family:'JetBrains Mono'; font-size:.65rem; color:var(--text-secondary);">MAU</div>
    <div style="font-family:'Playfair Display',serif; font-size:1.1rem; font-weight:900; color:var(--text-primary);">2.4M</div>
  </div>
  <div>
    <div style="font-family:'JetBrains Mono'; font-size:.65rem; color:var(--text-secondary);">GROWTH</div>
    <div style="font-family:'Playfair Display',serif; font-size:1.1rem; font-weight:900; color:var(--positive);">+276%</div>
  </div>
  <div>
    <div style="font-family:'JetBrains Mono'; font-size:.65rem; color:var(--text-secondary);">ARPU</div>
    <div style="font-family:'Playfair Display',serif; font-size:1.1rem; font-weight:900; color:var(--text-primary);">$4.2</div>
  </div>
</div>
```


---

## 交互效果类组件

### 32. CoolMode 按钮（点击粒子爆发）

点击时从按钮位置喷射彩色粒子，增加互动趣味性。适合CTA按钮、结尾页。

```html
<!-- HTML -->
<button class="cool-btn" onclick="coolBurst(event)">
  点击体验 →
</button>

<!-- CSS -->
<style>
.cool-btn {
  position: relative;
  background: var(--accent);
  color: #fff;
  border: none;
  padding: 14px 32px;
  border-radius: 8px;
  font-size: .9rem;
  font-weight: 700;
  cursor: pointer;
  transition: transform .2s, box-shadow .2s;
  font-family: 'Noto Sans SC', sans-serif;
}
.cool-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(0,0,0,.15);
}
.cool-btn:active { transform: scale(.96); }
.particle {
  position: fixed;
  pointer-events: none;
  border-radius: 50%;
  animation: particle-fly .8s ease-out forwards;
}
@keyframes particle-fly {
  0% { opacity: 1; transform: translate(0,0) scale(1); }
  100% { opacity: 0; transform: translate(var(--tx), var(--ty)) scale(0); }
}
</style>

<!-- JS -->
<script>
function coolBurst(e) {
  const colors = ['#ffb300','#3b82f6','#10b981','#ef4444','#8b5cf6','#f59e0b'];
  const rect = e.target.getBoundingClientRect();
  const cx = rect.left + rect.width/2;
  const cy = rect.top + rect.height/2;
  for(let i=0; i<20; i++){
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random()*8+4;
    const angle = Math.random()*Math.PI*2;
    const dist = Math.random()*100+50;
    p.style.width = size+'px';
    p.style.height = size+'px';
    p.style.left = cx+'px';
    p.style.top = cy+'px';
    p.style.background = colors[Math.floor(Math.random()*colors.length)];
    p.style.setProperty('--tx', Math.cos(angle)*dist+'px');
    p.style.setProperty('--ty', Math.sin(angle)*dist-40+'px');
    p.style.animationDuration = (Math.random()*.4+.5)+'s';
    document.body.appendChild(p);
    setTimeout(()=>p.remove(), 1000);
  }
}
</script>
```

### 33. InteractiveHoverButton（方向感知填充）

Hover时有颜色从鼠标进入方向填充的效果。适合导航按钮、标签切换。

```html
<!-- HTML -->
<button class="hover-fill-btn" onmouseenter="hoverFillEnter(event)" onmouseleave="hoverFillLeave(event)">
  <span class="hover-fill-bg"></span>
  <span class="hover-fill-text">Hover Me</span>
</button>

<!-- CSS -->
<style>
.hover-fill-btn {
  position: relative;
  overflow: hidden;
  background: transparent;
  border: 2px solid var(--accent);
  color: var(--accent);
  padding: 12px 28px;
  border-radius: 8px;
  font-size: .85rem;
  font-weight: 700;
  cursor: pointer;
  font-family: 'Noto Sans SC', sans-serif;
  transition: color .3s;
}
.hover-fill-btn:hover { color: #fff; }
.hover-fill-bg {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: var(--accent);
  transform: translateX(-101%);
  transition: transform .35s cubic-bezier(.4,0,.2,1);
  z-index: 0;
}
.hover-fill-btn:hover .hover-fill-bg { transform: translateX(0); }
.hover-fill-text { position: relative; z-index: 1; }
</style>

<!-- JS（方向感知版本） -->
<script>
function hoverFillEnter(e) {
  const bg = e.currentTarget.querySelector('.hover-fill-bg');
  const rect = e.currentTarget.getBoundingClientRect();
  const x = e.clientX - rect.left;
  if (x < rect.width/2) {
    bg.style.transform = 'translateX(-101%)';
    requestAnimationFrame(()=>{ bg.style.transition='none'; bg.style.transform='translateX(-101%)';
      requestAnimationFrame(()=>{ bg.style.transition='transform .35s cubic-bezier(.4,0,.2,1)'; bg.style.transform='translateX(0)'; });
    });
  } else {
    bg.style.transform = 'translateX(101%)';
    requestAnimationFrame(()=>{ bg.style.transition='none'; bg.style.transform='translateX(101%)';
      requestAnimationFrame(()=>{ bg.style.transition='transform .35s cubic-bezier(.4,0,.2,1)'; bg.style.transform='translateX(0)'; });
    });
  }
}
function hoverFillLeave(e) {
  const bg = e.currentTarget.querySelector('.hover-fill-bg');
  const rect = e.currentTarget.getBoundingClientRect();
  const x = e.clientX - rect.left;
  bg.style.transform = x < rect.width/2 ? 'translateX(-101%)' : 'translateX(101%)';
}
</script>
```

---

## 动态文字效果

### 34. KineticText（逐字符波动入场）

文字逐字符依次入场并带有弹性波动效果。适合封面页大标题、金句页。

```html
<!-- HTML -->
<div class="kinetic-text" data-text="AI漫剧时代">AI漫剧时代</div>

<!-- CSS -->
<style>
.kinetic-text {
  font-family: 'Playfair Display', serif;
  font-size: clamp(3rem, 8vw, 6rem);
  font-weight: 900;
  color: var(--text-primary);
  display: flex;
  justify-content: center;
  overflow: hidden;
}
.kinetic-text .char {
  display: inline-block;
  opacity: 0;
  transform: translateY(40px) rotateX(-40deg);
  animation: kinetic-in .6s cubic-bezier(.34,1.56,.64,1) forwards;
}
@keyframes kinetic-in {
  to { opacity: 1; transform: translateY(0) rotateX(0); }
}
</style>

<!-- JS（slide.active时触发） -->
<script>
document.querySelectorAll('.kinetic-text').forEach(el => {
  const text = el.textContent;
  el.innerHTML = '';
  [...text].forEach((char, i) => {
    const span = document.createElement('span');
    span.className = 'char';
    span.textContent = char === ' ' ? '\u00A0' : char;
    span.style.animationDelay = (i * 0.06) + 's';
    el.appendChild(span);
  });
});
</script>
```

### 35. ComicText（漫画描边爆裂文字）

粗体+多层描边+旋转微倾，像漫画音效文字。适合强调页、惊喜时刻。

```html
<!-- HTML -->
<div class="comic-text">BOOM!</div>

<!-- CSS -->
<style>
.comic-text {
  font-family: 'Playfair Display', serif;
  font-size: clamp(4rem, 12vw, 8rem);
  font-weight: 900;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: -2px;
  position: relative;
  display: inline-block;
  transform: rotate(-2deg);
  /* 多层text-shadow模拟描边 */
  text-shadow:
    3px 3px 0 var(--text-primary),
    -1px -1px 0 var(--text-primary),
    1px -1px 0 var(--text-primary),
    -1px 1px 0 var(--text-primary),
    0 4px 0 rgba(0,0,0,.15);
  /* 入场动画 */
  animation: comic-pop .5s cubic-bezier(.34,1.56,.64,1);
}
@keyframes comic-pop {
  0% { transform: rotate(-2deg) scale(0); opacity: 0; }
  60% { transform: rotate(-2deg) scale(1.15); }
  100% { transform: rotate(-2deg) scale(1); opacity: 1; }
}

/* 变体：无描边纯色版 */
.comic-text-clean {
  font-family: 'Playfair Display', serif;
  font-size: clamp(3rem, 10vw, 6rem);
  font-weight: 900;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: -1px;
  -webkit-text-stroke: 3px var(--text-primary);
  paint-order: stroke fill;
  animation: comic-pop .5s cubic-bezier(.34,1.56,.64,1);
}
</style>
```


### 36. Sparkles Text 星光文字

文字周围随机闪烁星星粒子。适合封面hero大标题、品牌名、金句强调。

```html
<!-- HTML -->
<div class="sparkle-wrap">
  <span class="sparkle-text">创造力</span>
</div>

<!-- CSS -->
<style>
.sparkle-wrap {
  position: relative;
  display: inline-block;
}
.sparkle-text {
  font-family: 'Playfair Display', serif;
  font-size: clamp(3rem, 8vw, 5rem);
  font-weight: 900;
  color: var(--accent);
  position: relative;
  z-index: 1;
}
.sparkle-star {
  position: absolute;
  pointer-events: none;
  animation: sparkle-anim 1.5s ease-in-out infinite;
}
@keyframes sparkle-anim {
  0%, 100% { opacity: 0; transform: scale(0) rotate(0deg); }
  50% { opacity: 1; transform: scale(1) rotate(180deg); }
}
</style>

<!-- JS -->
<script>
function initSparkles(el) {
  const wrap = el;
  const colors = ['#ffb300','#3b82f6','#e84a5f','#10b981'];
  setInterval(() => {
    const star = document.createElement('svg');
    star.className = 'sparkle-star';
    star.setAttribute('width','16');
    star.setAttribute('height','16');
    star.setAttribute('viewBox','0 0 24 24');
    star.innerHTML = '<path d="M12 0l3 9h9l-7 5 3 9-8-6-8 6 3-9-7-5h9z" fill="'+colors[Math.floor(Math.random()*colors.length)]+'"/>';
    star.style.left = Math.random()*100+'%';
    star.style.top = Math.random()*100+'%';
    star.style.animationDuration = (Math.random()*1+1)+'s';
    star.style.animationDelay = Math.random()*0.5+'s';
    wrap.appendChild(star);
    setTimeout(()=>star.remove(), 2000);
  }, 300);
}
document.querySelectorAll('.sparkle-wrap').forEach(initSparkles);
</script>
```

### 37. Typing Animation 打字机动画

文字逐字出现带闪烁光标效果。适合hero大标题、首屏大标语、slogan轮播。

```html
<!-- HTML -->
<div class="typing-text" data-text="Building the future with AI">
  <span class="typing-content"></span>
  <span class="typing-cursor">|</span>
</div>

<!-- CSS -->
<style>
.typing-text {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.8rem, 4vw, 3rem);
  font-weight: 900;
  color: var(--text-primary);
}
.typing-cursor {
  color: var(--accent);
  animation: blink .8s step-end infinite;
  font-weight: 300;
}
@keyframes blink {
  50% { opacity: 0; }
}
</style>

<!-- JS -->
<script>
function initTyping(el) {
  const text = el.dataset.text;
  const content = el.querySelector('.typing-content');
  let i = 0;
  content.textContent = '';
  const interval = setInterval(() => {
    if(i < text.length) {
      content.textContent += text[i];
      i++;
    } else {
      clearInterval(interval);
    }
  }, 80);
}
document.querySelectorAll('.typing-text').forEach(initTyping);
</script>
```


---

## 来自 Esther Design System 的适配组件

### 38. Morphing Text 文字变形（slogan轮播）

多个词语之间平滑切换变形。适合封面页slogan、hero区域。

```html
<div class="morph-text" style="font-family:'Playfair Display',serif; font-size:clamp(2rem,5vw,3.5rem); font-weight:900; color:var(--text-primary); text-align:center; min-height:1.2em;">
  <span class="morph-word active">创造力</span>
  <span class="morph-word">想象力</span>
  <span class="morph-word">执行力</span>
</div>
<style>
.morph-word { position:absolute; opacity:0; transition:opacity .6s, filter .6s; filter:blur(4px); }
.morph-word.active { position:relative; opacity:1; filter:blur(0); }
</style>
<script>
// 每2秒切换一个词
setInterval(()=>{
  const words = document.querySelectorAll('.morph-word');
  const active = document.querySelector('.morph-word.active');
  const idx = [...words].indexOf(active);
  active.classList.remove('active');
  words[(idx+1)%words.length].classList.add('active');
}, 2000);
</script>
```

### 39. 杂志裁切风卡片

大标题+描述+底部英文标签，像杂志内页的裁切板块。适合功能展示、核心卖点。

```html
<div style="display:grid; grid-template-columns:1fr 1fr; gap:20px;">
  <div style="padding:32px; border:1px solid var(--divider); border-radius:0;">
    <h3 style="font-family:'Playfair Display',serif; font-size:1.3rem; font-weight:900; color:var(--text-primary); margin-bottom:10px;">核心观点标题</h3>
    <p style="font-size:.8rem; color:var(--text-secondary); line-height:1.7; margin-bottom:16px;">描述文字，解释这个观点的具体含义和支撑逻辑。</p>
    <span style="font-family:'JetBrains Mono'; font-size:.65rem; color:var(--text-secondary); letter-spacing:1px; text-transform:uppercase;">CATEGORY-LABEL</span>
  </div>
</div>
```

### 40. 编号主导卡片

大编号+标题+描述，编号作为视觉主体。适合步骤列表、要点展示。

```html
<div style="display:grid; grid-template-columns:repeat(3,1fr); gap:16px;">
  <div style="padding:28px 24px;">
    <div style="font-family:'Playfair Display',serif; font-size:2.5rem; font-weight:900; color:var(--accent); opacity:.7; margin-bottom:8px;">01</div>
    <h4 style="font-size:.95rem; font-weight:700; color:var(--text-primary); margin-bottom:6px;">步骤标题</h4>
    <p style="font-size:.75rem; color:var(--text-secondary); line-height:1.6;">描述内容</p>
  </div>
</div>
```

### 41. 对话气泡

模拟聊天对话，我说+AI回。适合展示AI交互、用户反馈。

```html
<div style="display:flex; flex-direction:column; gap:12px; max-width:500px;">
  <!-- 用户(右对齐) -->
  <div style="align-self:flex-end; background:#fff; padding:12px 18px; border-radius:16px 16px 4px 16px; box-shadow:0 2px 8px rgba(0,0,0,.04); max-width:75%;">
    <p style="font-size:.8rem; color:var(--text-primary);">用户说的话</p>
  </div>
  <!-- AI(左对齐) -->
  <div style="align-self:flex-start; background:var(--accent-bg); padding:12px 18px; border-radius:16px 16px 16px 4px; max-width:75%;">
    <p style="font-size:.8rem; color:var(--text-secondary);">AI的回复</p>
  </div>
</div>
```

### 42. Do/Don't 对比

正反例对比展示。适合规范说明、方案对比。

```html
<div style="display:grid; grid-template-columns:1fr 1fr; gap:20px;">
  <div style="padding:24px; border-top:3px solid var(--negative);">
    <div style="font-size:.75rem; font-weight:700; color:var(--negative); margin-bottom:12px;">DON'T</div>
    <div style="font-size:.8rem; color:var(--text-secondary); line-height:1.8;">
      <span style="color:var(--negative);">✕</span> 错误做法一<br>
      <span style="color:var(--negative);">✕</span> 错误做法二
    </div>
  </div>
  <div style="padding:24px; border-top:3px solid var(--positive);">
    <div style="font-size:.75rem; font-weight:700; color:var(--positive); margin-bottom:12px;">DO</div>
    <div style="font-size:.8rem; color:var(--text-secondary); line-height:1.8;">
      <span style="color:var(--positive);">✓</span> 正确做法一<br>
      <span style="color:var(--positive);">✓</span> 正确做法二
    </div>
  </div>
</div>
```

### 43. 报纸多栏排版

高信息密度的多栏文字排版，像报纸。适合数据报告内容页。

```html
<div style="column-count:2; column-gap:32px; column-rule:1px solid var(--divider); font-size:.8rem; color:var(--text-secondary); line-height:1.8;">
  <h3 style="font-size:1.1rem; font-weight:900; color:var(--text-primary); margin-bottom:8px; column-span:all;">多栏标题</h3>
  <p>第一段内容...</p>
  <p style="margin-top:12px;">第二段内容...</p>
</div>
```

### 44. 全屏大片压字封面

深色背景+超大文字叠加。适合封面、章节分隔。

```html
<div style="background:var(--bg-dark-start); width:100%; height:100%; display:flex; align-items:flex-end; padding:60px 80px;">
  <div>
    <div style="font-family:'Playfair Display',serif; font-size:clamp(3rem,8vw,6rem); font-weight:900; color:#fff; line-height:1.1; margin-bottom:16px;">The Art of<br>Simplicity.</div>
    <div style="font-size:.8rem; color:var(--text-dark-secondary); letter-spacing:1px;">SUBTITLE — 用最少的元素传达最强的信息</div>
  </div>
</div>
```

### 45. Tab切换面板

点击标签切换内容区域。适合多维度数据分类展示。

```html
<div>
  <div style="display:flex; gap:0; border-bottom:1px solid var(--divider); margin-bottom:20px;">
    <button style="padding:10px 20px; border:none; background:none; font-size:.82rem; font-weight:600; color:var(--accent); border-bottom:2px solid var(--accent); cursor:pointer;">标签一</button>
    <button style="padding:10px 20px; border:none; background:none; font-size:.82rem; color:var(--text-secondary); cursor:pointer;">标签二</button>
    <button style="padding:10px 20px; border:none; background:none; font-size:.82rem; color:var(--text-secondary); cursor:pointer;">标签三</button>
  </div>
  <div style="font-size:.85rem; color:var(--text-secondary); line-height:1.8;">标签一的内容区域...</div>
</div>
```

### 46. 手风琴展开

点击展开/收起详细内容。适合FAQ、详细说明。

```html
<div style="border:1px solid var(--divider); border-radius:8px; overflow:hidden;">
  <div style="padding:16px 20px; cursor:pointer; display:flex; justify-content:space-between; align-items:center; background:#fff;">
    <span style="font-size:.88rem; font-weight:600; color:var(--text-primary);">问题标题</span>
    <span style="color:var(--text-secondary);">▼</span>
  </div>
  <div style="padding:0 20px 16px; font-size:.8rem; color:var(--text-secondary); line-height:1.7;">展开后的详细内容...</div>
</div>
```

### 47. Section Header 大编号章节标题

超大装饰编号+章节标题。适合章节分隔。

```html
<div style="display:flex; align-items:baseline; gap:16px;">
  <span style="font-family:'Playfair Display',serif; font-size:clamp(3rem,8vw,5rem); font-weight:900; color:var(--accent); opacity:.3; line-height:1;">01</span>
  <h2 style="font-size:clamp(1.4rem,3vw,2rem); font-weight:900; color:var(--text-primary);">章节标题</h2>
</div>
```

### 48. 横向时间线

水平方向的阶段/里程碑展示。适合述职、项目进度。

```html
<div style="display:flex; gap:0; align-items:flex-start;">
  <div style="flex:1; text-align:center; position:relative;">
    <div style="width:12px; height:12px; border-radius:50%; background:var(--accent); margin:0 auto 10px;"></div>
    <div style="position:absolute; top:5px; left:50%; width:100%; height:2px; background:var(--divider); z-index:-1;"></div>
    <div style="font-size:.72rem; font-weight:600; color:var(--text-primary);">Phase 1</div>
    <div style="font-size:.68rem; color:var(--text-secondary); margin-top:4px;">探索期</div>
  </div>
  <!-- 重复更多节点 -->
</div>
```

### 49. 圆形步骤循环

环形排列的循环步骤。适合闭环逻辑展示。

```html
<div style="display:flex; align-items:center; justify-content:center; gap:8px; flex-wrap:wrap;">
  <div style="text-align:center; padding:12px;">
    <div style="width:48px; height:48px; border-radius:50%; background:var(--accent-bg); display:flex; align-items:center; justify-content:center; margin:0 auto 8px; font-size:1.2rem;">💡</div>
    <div style="font-size:.7rem; font-weight:600; color:var(--text-primary);">想法</div>
  </div>
  <span style="font-size:.8rem; color:var(--text-secondary);">›</span>
  <!-- 重复更多步骤，最后一个用 ⟳ 回到第一个 -->
</div>
```

### 50. Pull Quote 大字引用

超大引号+黄色边框包围+粗体引用文字。适合金句页。

```html
<div style="border:2px solid var(--accent); border-radius:12px; padding:32px 28px; position:relative; max-width:600px;">
  <div style="font-family:'Playfair Display',serif; font-size:2rem; color:var(--accent); position:absolute; top:16px; left:20px; line-height:1; opacity:.6;">❝</div>
  <p style="font-family:'Noto Sans SC',sans-serif; font-size:1.05rem; font-weight:700; color:var(--text-primary); line-height:1.8; padding-left:8px; margin-top:12px;">
    引用文字内容，用完整的句子。少即是多——不是做减法的借口，而是每一个元素都必须证明自己存在的价值。
  </p>
</div>
```

### 51. 手写批注风引用（Key Insight）

黄色虚线边框+Caveat手写标签浮在边框上方。适合结论强调。

```html
<div style="border:1.5px dashed var(--accent); border-radius:8px; padding:24px 20px; position:relative;">
  <span style="font-family:'Caveat',cursive; font-size:1.05rem; color:var(--accent); position:absolute; top:-12px; left:16px; background:#fff; padding:0 8px;">Key Insight ✦</span>
  <p style="font-size:.88rem; color:var(--text-primary); line-height:1.8; margin-top:4px;">
    核心洞察内容，用完整的句子描述关键发现。
  </p>
</div>
```

### 52. 对比表（圆点标识简洁风）

简洁的多维度对比，用圆点标识优劣。适合方案/竞品对比。

```html
<div style="display:flex; flex-direction:column; gap:0;">
  <div style="display:flex; align-items:center; padding:14px 0; border-bottom:1px solid var(--divider);">
    <span style="flex:1; font-size:.82rem; font-weight:600; color:var(--text-primary);">维度名称</span>
    <span style="flex:1; font-size:.78rem; color:var(--text-secondary);">方案A描述</span>
    <span style="flex:1; font-size:.78rem; color:var(--accent); font-weight:600;">方案B描述</span>
  </div>
  <!-- 重复更多行 -->
</div>
```

### 53. 悬停揭示卡片

默认显示标题，hover显示详细释义。适合名词解释、概念展示。

```html
<div style="padding:32px; text-align:center; cursor:pointer; transition:all .3s;" onmouseover="this.querySelector('.reveal').style.opacity='1';this.querySelector('.reveal').style.transform='translateY(0)'" onmouseout="this.querySelector('.reveal').style.opacity='0';this.querySelector('.reveal').style.transform='translateY(8px)'">
  <h3 style="font-family:'Playfair Display',serif; font-size:1.8rem; font-weight:900; color:var(--text-primary); margin-bottom:12px;">概念名称</h3>
  <div class="reveal" style="font-size:.82rem; color:var(--text-secondary); line-height:1.7; opacity:0; transform:translateY(8px); transition:all .3s;">
    悬停后显示的详细解释文字...
  </div>
</div>
```

### 54. 编号卡片网格

4格并列，每格带编号+标题+描述。适合并列任务、4个要点。

```html
<div style="display:grid; grid-template-columns:1fr 1fr; gap:16px;">
  <div style="padding:20px; border:1px solid var(--divider);">
    <span style="font-family:'Playfair Display',serif; font-size:1.4rem; font-weight:900; color:var(--accent); opacity:.6;">01</span>
    <h4 style="font-size:.88rem; font-weight:700; color:var(--text-primary); margin:8px 0 4px;">标题</h4>
    <p style="font-size:.72rem; color:var(--text-secondary); line-height:1.6;">描述</p>
  </div>
  <!-- 重复4格 -->
</div>
```

### 55. Text Highlighter 手绘标注

正文中多处用手绘风格高亮。适合强调多个关键词。

```html
<p style="font-size:.9rem; color:var(--text-primary); line-height:2;">
  在设计系统中，<span style="background:linear-gradient(transparent 55%, var(--accent-light) 55%); padding:0 3px;">一致性比创新更重要</span>。
  每个组件都要证明价值——如果一个元素无法提升体验就该<span style="background:linear-gradient(transparent 55%, var(--accent-light) 55%); padding:0 3px;">删掉</span>。
  记住：<span style="background:linear-gradient(transparent 55%, rgba(239,83,80,.2) 55%); padding:0 3px; font-weight:700;">少即是多</span>。
</p>
```


---

## 数据图表类组件（Chart.js）

> 凡是有数据对比/趋势/分布/占比的内容，**必须画图**，不能只用文字。使用 Chart.js CDN 或纯 SVG 绘制现代风格图表。

### 图表全局规则

1. **引入 Chart.js**（在 `<head>` 中加一次即可）：
```html
<script src="https://cdn.jsdelivr.net/npm/chart.js@4/dist/chart.umd.min.js"></script>
```

2. **风格要求**：
   - 圆角柱状图（`borderRadius: 6`）
   - 渐变或半透明填充（不要实心纯色块）
   - 无网格线或极淡网格（`grid: { color: 'rgba(0,0,0,.04)' }`）
   - 隐藏坐标轴线（`border: { display: false }`）
   - 字体使用 Noto Sans SC（`Chart.defaults.font.family = 'Noto Sans SC'`）
   - tooltip 圆角+阴影
   - legend 放底部或隐藏（数据系列≤2时隐藏）

3. **配色规则**（跟随当前主题）：
   - 暖彩三色主题：青绿 `#438C80` / 玫瑰 `#DE8784` / 暖金 `#E1BC8B`
   - 深空蓝主题：蓝 `#3b82f6` / 绿 `#10b981` / 红 `#ef4444`
   - 渐变示例：`ctx.createLinearGradient(0, 0, 0, 300)` → 主色到透明

4. **canvas 容器样式**：
```html
<div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 2px 12px rgba(0,0,0,.04); position:relative;">
  <canvas id="chartX" style="width:100%; max-height:280px;"></canvas>
</div>
```

---

### 56. 柱状图（对比类）

适合：多组数据对比、同比环比、人群分组对比

```html
<div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="barChart1"></canvas>
</div>
<script>
new Chart(document.getElementById('barChart1'), {
  type: 'bar',
  data: {
    labels: ['正向人群', '中性人群', '负向人群'],
    datasets: [{
      label: '喂奶达成率',
      data: [30.8, 12.4, 0.6],
      backgroundColor: ['#438C80', '#E1BC8B', '#DE8784'],
      borderRadius: 6,
      barThickness: 36
    }]
  },
  options: {
    responsive: true,
    plugins: { legend: { display: false } },
    scales: {
      y: { grid: { color: 'rgba(0,0,0,.04)' }, border: { display: false }, ticks: { font: { size: 11 } } },
      x: { grid: { display: false }, border: { display: false }, ticks: { font: { size: 11 } } }
    }
  }
});
</script>
```

### 57. 折线图（趋势类）

适合：时间序列、趋势变化、投诉后达成变化

```html
<div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="lineChart1"></canvas>
</div>
<script>
(function(){
  const ctx = document.getElementById('lineChart1').getContext('2d');
  const gradient = ctx.createLinearGradient(0, 0, 0, 250);
  gradient.addColorStop(0, 'rgba(67,140,128,.25)');
  gradient.addColorStop(1, 'rgba(67,140,128,.01)');
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: ['投诉前', '次日', 'D2', 'D3', 'D4', 'D5', 'D6', 'D7'],
      datasets: [{
        label: '人均达成',
        data: [100, 61, 63, 60, 62, 58, 61, 60],
        borderColor: '#438C80',
        backgroundColor: gradient,
        fill: true,
        tension: 0.4,
        pointRadius: 4,
        pointBackgroundColor: '#438C80'
      }]
    },
    options: {
      responsive: true,
      plugins: { legend: { display: false } },
      scales: {
        y: { grid: { color: 'rgba(0,0,0,.04)' }, border: { display: false } },
        x: { grid: { display: false }, border: { display: false } }
      }
    }
  });
})();
</script>
```

### 58. 环形图（占比类）

适合：构成分析、原因分布、市场份额

```html
<div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 2px 12px rgba(0,0,0,.04); display:flex; align-items:center; gap:24px;">
  <div style="width:180px; height:180px; position:relative;">
    <canvas id="doughnut1"></canvas>
  </div>
  <div style="display:flex; flex-direction:column; gap:10px;">
    <div style="display:flex; align-items:center; gap:8px;">
      <div style="width:10px; height:10px; border-radius:3px; background:#438C80;"></div>
      <span style="font-size:.78rem; color:var(--text-primary);">多Boss触达 40%</span>
    </div>
    <div style="display:flex; align-items:center; gap:8px;">
      <div style="width:10px; height:10px; border-radius:3px; background:#DE8784;"></div>
      <span style="font-size:.78rem; color:var(--text-primary);">拒后仍推 30%</span>
    </div>
    <div style="display:flex; align-items:center; gap:8px;">
      <div style="width:10px; height:10px; border-radius:3px; background:#E1BC8B;"></div>
      <span style="font-size:.78rem; color:var(--text-primary);">排斥类型 15%</span>
    </div>
    <div style="display:flex; align-items:center; gap:8px;">
      <div style="width:10px; height:10px; border-radius:3px; background:#ccc;"></div>
      <span style="font-size:.78rem; color:var(--text-primary);">其他 15%</span>
    </div>
  </div>
</div>
<script>
new Chart(document.getElementById('doughnut1'), {
  type: 'doughnut',
  data: {
    labels: ['多Boss触达', '拒后仍推', '排斥类型', '其他'],
    datasets: [{
      data: [40, 30, 15, 15],
      backgroundColor: ['#438C80', '#DE8784', '#E1BC8B', '#ddd'],
      borderWidth: 0,
      cutout: '65%'
    }]
  },
  options: {
    responsive: true,
    plugins: { legend: { display: false } }
  }
});
</script>
```

### 59. 分组柱状图（AB对比类）

适合：实验组vs对照组、前后对比、多维度对比

```html
<div style="background:#fff; border-radius:14px; padding:24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="groupBar1"></canvas>
</div>
<script>
new Chart(document.getElementById('groupBar1'), {
  type: 'bar',
  data: {
    labels: ['人均达成', '7日留存', '投诉率'],
    datasets: [
      { label: '实验组', data: [2.4, 78, 1.2], backgroundColor: '#438C80', borderRadius: 6 },
      { label: '对照组', data: [1.8, 72, 2.8], backgroundColor: '#E1BC8B', borderRadius: 6 }
    ]
  },
  options: {
    responsive: true,
    plugins: { legend: { position: 'bottom', labels: { font: { size: 11 } } } },
    scales: {
      y: { grid: { color: 'rgba(0,0,0,.04)' }, border: { display: false } },
      x: { grid: { display: false }, border: { display: false } }
    }
  }
});
</script>
```

### 60. 纯SVG迷你图（内嵌在数据行中）

适合：数据行内展示趋势，不需要完整图表时的迷你可视化

```html
<!-- 迷你趋势线（纯SVG，无依赖） -->
<svg width="80" height="24" viewBox="0 0 80 24" fill="none" style="vertical-align:middle;">
  <polyline points="2,20 15,16 28,18 40,10 52,12 65,6 78,4" stroke="#438C80" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" fill="none"/>
  <circle cx="78" cy="4" r="3" fill="#438C80"/>
</svg>

<!-- 迷你柱状图 -->
<svg width="60" height="24" viewBox="0 0 60 24" fill="none" style="vertical-align:middle;">
  <rect x="2" y="12" width="8" height="12" rx="2" fill="#E1BC8B"/>
  <rect x="14" y="8" width="8" height="16" rx="2" fill="#E1BC8B"/>
  <rect x="26" y="4" width="8" height="20" rx="2" fill="#438C80"/>
  <rect x="38" y="6" width="8" height="18" rx="2" fill="#438C80"/>
  <rect x="50" y="2" width="8" height="22" rx="2" fill="#438C80"/>
</svg>
```

---

## 图表选择决策表

> 根据数据类型自动选择最合适的图表，**不允许跳过图表只写文字**。

| 数据场景 | 推荐图表 | 组件编号 |
|---------|---------|---------|
| 多组数值对比（人群/方案/指标） | 柱状图 | 61 |
| 时间序列/趋势变化 | 折线面积图 | 62 |
| 构成/占比/原因分布 | 环形图 | 63 |
| AB测试/实验对照/前后对比 | 分组柱状图 | 64 |
| 模型效果迭代/阶段性下降 | 面积折线图 | 65 |
| 人群画像/多维特征 | 横向柱状图 | 66 |
| 两组指标反向变化趋势 | 双折线图 | 67 |
| 调控前后资源重分配 | 前后对比柱状图 | 68 |
| 行内迷你趋势（不需独立图表） | SVG迷你图 | 60 |

### 图表插入规则

1. 图表作为**插图**嵌入PPT页面，与文字内容混排（左图右文 或 上图下洞察）
2. 图表容器统一样式：白底 + 圆角14px + 轻阴影
3. 图表下方/旁边**必须有洞察条**解读
4. 一页最多放2个图表（1主1辅），超过则分页
5. Canvas 高度控制在 200-280px，不要过大抢占文字空间

---

### 61. 柱状图（多组对比）

适合：人群分层对比、多指标并列、评分分布

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="barChartX" style="max-height:240px;"></canvas>
</div>
<script>
new Chart(document.getElementById('barChartX'), {
  type: 'bar',
  data: {
    labels: ['正向人群', '中性人群', '负向人群'],
    datasets: [{
      data: [30.8, 12.4, 0.6],
      backgroundColor: ['#438C80', '#E1BC8B', '#DE8784'],
      borderRadius: 8,
      barThickness: 42
    }]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    plugins: { legend: { display: false },
      tooltip: { backgroundColor:'#fff', titleColor:'#010005', bodyColor:'#666', borderColor:'#eee', borderWidth:1, cornerRadius:8, padding:12 }
    },
    scales: {
      y: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false }, ticks: { callback: v=>v+'%' } },
      x: { grid: { display:false }, border: { display:false } }
    }
  }
});
</script>
```

### 62. 折线面积图（趋势类）

适合：投诉后达成变化、日/周级时间序列、指标走势

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="lineChartX" style="max-height:240px;"></canvas>
</div>
<script>
(function(){
  const ctx = document.getElementById('lineChartX').getContext('2d');
  const g = ctx.createLinearGradient(0, 0, 0, 200);
  g.addColorStop(0, 'rgba(222,135,132,.2)');
  g.addColorStop(1, 'rgba(222,135,132,.01)');
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: ['投诉前','次日','D2','D3','D4','D5','D6','D7'],
      datasets: [{
        data: [100, 61, 63, 60, 62, 58, 61, 60],
        borderColor: '#DE8784',
        backgroundColor: g,
        fill: true,
        tension: 0.4,
        pointRadius: 5,
        pointBackgroundColor: '#DE8784',
        pointBorderColor: '#fff',
        pointBorderWidth: 2
      }]
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        y: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false }, min:40 },
        x: { grid: { display:false }, border: { display:false } }
      }
    }
  });
})();
</script>
```

### 63. 环形图（占比类）

适合：原因分布、市场构成、资源分配比例

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04); display:flex; align-items:center; gap:24px;">
  <div style="width:180px; height:180px;">
    <canvas id="doughnutX"></canvas>
  </div>
  <div style="display:flex; flex-direction:column; gap:10px;">
    <div style="display:flex;align-items:center;gap:8px;"><div style="width:12px;height:12px;border-radius:3px;background:#438C80;"></div><span style="font-size:.78rem;">多Boss触达 <strong>40%</strong></span></div>
    <div style="display:flex;align-items:center;gap:8px;"><div style="width:12px;height:12px;border-radius:3px;background:#DE8784;"></div><span style="font-size:.78rem;">拒后仍推 <strong>30%</strong></span></div>
    <div style="display:flex;align-items:center;gap:8px;"><div style="width:12px;height:12px;border-radius:3px;background:#E1BC8B;"></div><span style="font-size:.78rem;">排斥类型 <strong>15%</strong></span></div>
    <div style="display:flex;align-items:center;gap:8px;"><div style="width:12px;height:12px;border-radius:3px;background:#ddd;"></div><span style="font-size:.78rem;">其他 <strong>15%</strong></span></div>
  </div>
</div>
<script>
new Chart(document.getElementById('doughnutX'), {
  type: 'doughnut',
  data: {
    labels: ['多Boss触达','拒后仍推','排斥类型','其他'],
    datasets: [{ data:[40,30,15,15], backgroundColor:['#438C80','#DE8784','#E1BC8B','#e0e0e0'], borderWidth:0, cutout:'62%', borderRadius:4 }]
  },
  options: { responsive:true, plugins: { legend: { display:false } } }
});
</script>
```

### 64. 分组柱状图（AB对比）

适合：实验组vs对照组、方案对比、前后指标

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="groupBarX" style="max-height:240px;"></canvas>
</div>
<script>
new Chart(document.getElementById('groupBarX'), {
  type: 'bar',
  data: {
    labels: ['人均达成','7日留存','投诉率(‰)'],
    datasets: [
      { label:'实验组', data:[2.4,78,1.2], backgroundColor:'#438C80', borderRadius:6 },
      { label:'对照组', data:[1.8,72,2.8], backgroundColor:'#E1BC8B', borderRadius:6 }
    ]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    plugins: { legend: { position:'bottom', labels: { usePointStyle:true, pointStyle:'rectRounded', padding:16 } } },
    scales: {
      y: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false } },
      x: { grid: { display:false }, border: { display:false } }
    }
  }
});
</script>
```

### 65. 面积折线图（阶段下降/提升）

适合：模型迭代效果、成本优化过程、逐步改善

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="areaChartX" style="max-height:240px;"></canvas>
</div>
<script>
(function(){
  const ctx = document.getElementById('areaChartX').getContext('2d');
  const g = ctx.createLinearGradient(0,0,0,200);
  g.addColorStop(0,'rgba(67,140,128,.2)');
  g.addColorStop(1,'rgba(67,140,128,.01)');
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: ['V1 Baseline','V2 +打扰特征','V3 +倾向度'],
      datasets: [{
        data: [134, 64, 28],
        borderColor:'#438C80', backgroundColor:g, fill:true, tension:0.3,
        pointRadius:7, pointBackgroundColor:'#438C80', pointBorderColor:'#fff', pointBorderWidth:3
      }]
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { display:false } },
      scales: {
        y: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false }, ticks: { callback: v=>v+'%' } },
        x: { grid: { display:false }, border: { display:false } }
      }
    }
  });
})();
</script>
```

### 66. 横向柱状图（多维画像）

适合：人群画像、多维特征对比、满意度各项评分

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="hBarX" style="max-height:240px;"></canvas>
</div>
<script>
new Chart(document.getElementById('hBarX'), {
  type: 'bar',
  data: {
    labels: ['女性占比','行业HHI','标注勿扰','平均年龄'],
    datasets: [{
      data: [82, 53, 27, 24],
      backgroundColor: ['#DE8784','#438C80','#E1BC8B','#438C80'],
      borderRadius: 6, barThickness: 22
    }]
  },
  options: {
    indexAxis: 'y',
    responsive: true, maintainAspectRatio: false,
    plugins: { legend: { display:false } },
    scales: {
      x: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false } },
      y: { grid: { display:false }, border: { display:false } }
    }
  }
});
</script>
```

### 67. 双折线图（反向趋势）

适合：两组指标反向变化、增长vs下降同时展示

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="dualLineX" style="max-height:240px;"></canvas>
</div>
<script>
(function(){
  const ctx = document.getElementById('dualLineX').getContext('2d');
  const g1 = ctx.createLinearGradient(0,0,0,200); g1.addColorStop(0,'rgba(67,140,128,.15)'); g1.addColorStop(1,'rgba(67,140,128,.01)');
  const g2 = ctx.createLinearGradient(0,0,0,200); g2.addColorStop(0,'rgba(222,135,132,.15)'); g2.addColorStop(1,'rgba(222,135,132,.01)');
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: ['W1','W2','W3','W4','W5','W6'],
      datasets: [
        { label:'正向人群达成', data:[1.8,2.0,2.2,2.3,2.4,2.5], borderColor:'#438C80', backgroundColor:g1, fill:true, tension:0.4, pointRadius:5, pointBackgroundColor:'#438C80', pointBorderColor:'#fff', pointBorderWidth:2 },
        { label:'负向被打扰次数', data:[24,23,22,21,22,21], borderColor:'#DE8784', backgroundColor:g2, fill:true, tension:0.4, pointRadius:5, pointBackgroundColor:'#DE8784', pointBorderColor:'#fff', pointBorderWidth:2 }
      ]
    },
    options: {
      responsive: true, maintainAspectRatio: false,
      plugins: { legend: { position:'bottom', labels: { usePointStyle:true, pointStyle:'circle', padding:16 } } },
      scales: {
        y: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false } },
        x: { grid: { display:false }, border: { display:false } }
      }
    }
  });
})();
</script>
```

### 68. 前后对比柱状图（资源重分配）

适合：调控前后对比、预算重分配、产能变化

```html
<div style="background:#fff; border-radius:14px; padding:20px 24px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <canvas id="compareBarX" style="max-height:240px;"></canvas>
</div>
<script>
new Chart(document.getElementById('compareBarX'), {
  type: 'bar',
  data: {
    labels: ['负向人群','正向人群','总量'],
    datasets: [
      { label:'调控前', data:[3200,1800,5000], backgroundColor:'#E1BC8B', borderRadius:6 },
      { label:'调控后', data:[2832,1910,4850], backgroundColor:'#438C80', borderRadius:6 }
    ]
  },
  options: {
    responsive: true, maintainAspectRatio: false,
    plugins: { legend: { position:'bottom', labels: { usePointStyle:true, pointStyle:'rectRounded', padding:16 } } },
    scales: {
      y: { grid: { color:'rgba(0,0,0,.04)' }, border: { display:false } },
      x: { grid: { display:false }, border: { display:false } }
    }
  }
});
</script>
```


---

## 分析图表类组件（纯SVG/HTML）

> 以下图表适用于咨询风格的策略分析页面，使用纯SVG+HTML绘制，不依赖 Chart.js。

### 69. 阈值区间图（Threshold Zone Chart）

适合：成本阈值分析、分段决策、价格区间、风险分层。X轴为连续变量，用竖虚线标注关键阈值把区间切开，每段有不同语义。

```html
<!-- 阈值区间图：可替换阈值名称、曲线、区间标签 -->
<div style="background:#fff; border-radius:14px; padding:28px 32px; box-shadow:0 2px 12px rgba(0,0,0,.04); position:relative;">
  <!-- 标题 -->
  <div style="font-size:.78rem; font-weight:700; color:var(--text-primary); margin-bottom:6px;">成本与流失关系：确定心理可承受价上限（PP）</div>
  <div style="font-size:.68rem; color:var(--text-secondary); margin-bottom:20px;">通过复购率/续约率随实际成本变化，确定客户心理可承受价上限</div>

  <!-- SVG 图表主体 -->
  <svg viewBox="0 0 700 220" style="width:100%; height:auto;" xmlns="http://www.w3.org/2000/svg">
    <!-- 区间背景色块 -->
    <rect x="80" y="20" width="160" height="160" fill="rgba(67,140,128,.06)" rx="0"/>
    <rect x="240" y="20" width="200" height="160" fill="rgba(225,188,139,.06)" rx="0"/>
    <rect x="440" y="20" width="180" height="160" fill="rgba(222,135,132,.06)" rx="0"/>

    <!-- X轴 -->
    <line x1="60" y1="180" x2="640" y2="180" stroke="#ddd" stroke-width="1"/>
    <!-- Y轴 -->
    <line x1="60" y1="20" x2="60" y2="180" stroke="#ddd" stroke-width="1"/>

    <!-- 曲线（复购率从高到低） -->
    <path d="M80,40 C120,42 180,45 240,60 C300,80 380,120 440,150 C500,168 560,172 620,175" fill="none" stroke="#438C80" stroke-width="2.5" stroke-linecap="round"/>

    <!-- 阈值竖虚线 PA -->
    <line x1="130" y1="25" x2="130" y2="180" stroke="#438C80" stroke-width="1.5" stroke-dasharray="4,3"/>
    <text x="130" y="198" text-anchor="middle" font-size="11" font-weight="700" fill="#438C80">PA</text>
    <text x="130" y="212" text-anchor="middle" font-size="9" fill="#666">当前实际成本</text>

    <!-- 阈值竖虚线 PR -->
    <line x1="310" y1="25" x2="310" y2="180" stroke="#E1BC8B" stroke-width="1.5" stroke-dasharray="4,3"/>
    <text x="310" y="198" text-anchor="middle" font-size="11" font-weight="700" fill="#E1BC8B">PR</text>
    <text x="310" y="212" text-anchor="middle" font-size="9" fill="#666">行业成本警戒线</text>

    <!-- 阈值竖虚线 PP -->
    <line x1="490" y1="25" x2="490" y2="180" stroke="#DE8784" stroke-width="1.5" stroke-dasharray="4,3"/>
    <text x="490" y="198" text-anchor="middle" font-size="11" font-weight="700" fill="#DE8784">PP</text>
    <text x="490" y="212" text-anchor="middle" font-size="9" fill="#666">心理可承受上限</text>

    <!-- 区间标签 -->
    <text x="160" y="12" text-anchor="middle" font-size="10" font-weight="600" fill="#438C80">亏区</text>
    <text x="350" y="12" text-anchor="middle" font-size="10" font-weight="600" fill="#E1BC8B">可提价优化区</text>
    <text x="540" y="12" text-anchor="middle" font-size="10" font-weight="600" fill="#DE8784">承压流失区</text>

    <!-- Y轴标签 -->
    <text x="12" y="45" font-size="9" fill="#666">高</text>
    <text x="12" y="175" font-size="9" fill="#666">低</text>
    <text x="8" y="105" font-size="9" fill="#666" writing-mode="tb">复购率/续约率</text>

    <!-- 关键标注箭头（可提价空间） -->
    <line x1="160" y1="85" x2="280" y2="85" stroke="#E1BC8B" stroke-width="2" marker-end="url(#arrowGold)"/>
    <text x="220" y="78" text-anchor="middle" font-size="9" font-weight="600" fill="#E1BC8B">提价优化空间</text>

    <!-- 箭头marker -->
    <defs>
      <marker id="arrowGold" markerWidth="8" markerHeight="8" refX="7" refY="4" orient="auto">
        <path d="M0,0 L8,4 L0,8 Z" fill="#E1BC8B"/>
      </marker>
    </defs>
  </svg>

  <!-- 右侧关键结论（用绝对定位或flex） -->
  <div style="position:absolute; right:32px; top:50%; transform:translateY(-50%); max-width:160px;">
    <div style="font-size:.68rem; font-weight:700; color:var(--text-primary); margin-bottom:8px;">关键结论（阈值关系）</div>
    <div style="font-size:.72rem; color:var(--text-primary); line-height:1.8;">
      <strong style="color:#438C80;">PA</strong> &lt; <strong style="color:#E1BC8B;">PR</strong> &lt; <strong style="color:#DE8784;">PP</strong><br>
      存在亏，且具备提价空间；<br>
      超过PP后进入流失区
    </div>
  </div>
</div>
```

**使用时替换：**
- 阈值名称（PA/PR/PP → 你的阈值）
- 曲线path的d属性（根据实际数据趋势调整）
- 区间标签文字
- 右侧结论文字

---

### 70. 矩阵分区图 / 策略象限图（Matrix Zone Chart）

适合：双维度交叉分析、场景识别、客群×成本矩阵、风险矩阵。X轴和Y轴各代表一个维度，用色块标注不同策略区域，旁边附画像卡片。

```html
<!-- 矩阵分区图 -->
<div style="background:#fff; border-radius:14px; padding:28px 32px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <!-- 标题 -->
  <div style="font-size:.78rem; font-weight:700; color:var(--text-primary); margin-bottom:6px;">成本与需求量关系：识别三大流量价值错配场景</div>
  <div style="font-size:.68rem; color:var(--text-secondary); margin-bottom:20px;">结合需求下限（TD）与客群画像（K-means聚类），交叉识别亏/流失场景</div>

  <div style="display:flex; gap:24px;">
    <!-- 左侧：矩阵SVG -->
    <div style="flex:1.5;">
      <svg viewBox="0 0 500 320" style="width:100%; height:auto;" xmlns="http://www.w3.org/2000/svg">
        <!-- 坐标轴 -->
        <line x1="60" y1="260" x2="460" y2="260" stroke="#ddd" stroke-width="1"/>
        <line x1="60" y1="30" x2="60" y2="260" stroke="#ddd" stroke-width="1"/>

        <!-- 区间色块 -->
        <!-- 左下：超给亏 -->
        <rect x="61" y="140" width="130" height="119" fill="rgba(67,140,128,.08)" rx="0"/>
        <!-- 左上：边际亏 -->
        <rect x="61" y="31" width="130" height="109" fill="rgba(67,140,128,.15)" rx="0"/>
        <!-- 中间：可提价优化区 -->
        <rect x="191" y="31" width="140" height="228" fill="rgba(225,188,139,.08)" rx="0"/>
        <!-- 右侧：承压流失区 -->
        <rect x="331" y="31" width="128" height="228" fill="rgba(222,135,132,.1)" rx="0"/>

        <!-- 阈值竖虚线 -->
        <line x1="140" y1="30" x2="140" y2="260" stroke="#438C80" stroke-width="1.5" stroke-dasharray="4,3"/>
        <line x1="260" y1="30" x2="260" y2="260" stroke="#E1BC8B" stroke-width="1.5" stroke-dasharray="4,3"/>
        <line x1="390" y1="30" x2="390" y2="260" stroke="#DE8784" stroke-width="1.5" stroke-dasharray="4,3"/>

        <!-- 需求下限横虚线 TD -->
        <line x1="60" y1="140" x2="460" y2="140" stroke="#666" stroke-width="1" stroke-dasharray="3,3"/>
        <text x="48" y="144" text-anchor="end" font-size="9" fill="#666">TD</text>

        <!-- X轴标签 -->
        <text x="140" y="278" text-anchor="middle" font-size="10" font-weight="600" fill="#438C80">PA</text>
        <text x="260" y="278" text-anchor="middle" font-size="10" font-weight="600" fill="#E1BC8B">PR</text>
        <text x="390" y="278" text-anchor="middle" font-size="10" font-weight="600" fill="#DE8784">PP</text>
        <text x="260" y="300" text-anchor="middle" font-size="9" fill="#666">实际成本 / 达成单价 (PA)</text>

        <!-- Y轴标签 -->
        <text x="12" y="48" font-size="9" fill="#666">高</text>
        <text x="12" y="255" font-size="9" fill="#666">低</text>
        <text x="8" y="145" font-size="9" fill="#666" writing-mode="tb">客流量</text>

        <!-- 区域标注 -->
        <!-- ① 超给亏 -->
        <circle cx="105" cy="200" r="5" fill="#438C80"/>
        <text x="115" y="195" font-size="9" font-weight="600" fill="#438C80">① 超给亏</text>
        <text x="80" y="215" font-size="8" fill="#666">成本低但需求强</text>
        <text x="80" y="228" font-size="8" fill="#666">有较大提价空间</text>

        <!-- ② 边际亏 -->
        <circle cx="105" cy="80" r="5" fill="#438C80"/>
        <text x="115" y="75" font-size="9" font-weight="600" fill="#438C80">② 边际亏</text>
        <text x="80" y="95" font-size="8" fill="#666">流量给了但需求不强</text>
        <text x="80" y="108" font-size="8" fill="#666">超额价值趋于0</text>

        <!-- 可提价优化区 -->
        <text x="225" y="90" font-size="10" font-weight="600" fill="#E1BC8B">可提价</text>
        <text x="225" y="106" font-size="10" font-weight="600" fill="#E1BC8B">优化区</text>
        <text x="200" y="126" font-size="8" fill="#666">PR ≤ PA ≤ PP</text>
        <text x="200" y="140" font-size="8" fill="#666">可逐步缓慢提价</text>

        <!-- ③ 承压流失 -->
        <circle cx="365" cy="80" r="5" fill="#DE8784"/>
        <text x="375" y="75" font-size="9" font-weight="600" fill="#DE8784">③ 承压流失</text>
        <text x="345" y="95" font-size="8" fill="#666">PA &gt; PP</text>
        <text x="345" y="108" font-size="8" fill="#666">高断约风险</text>
      </svg>
    </div>

    <!-- 右侧：画像卡片 -->
    <div style="flex:.8; display:flex; flex-direction:column; gap:12px; justify-content:center;">
      <div style="font-size:.72rem; font-weight:700; color:var(--text-primary); margin-bottom:4px;">客群画像（聚类）</div>

      <div style="padding:12px 14px; border-left:3px solid #438C80; background:rgba(67,140,128,.04); border-radius:0 8px 8px 0;">
        <div style="font-size:.72rem; font-weight:700; color:#438C80;">批量型（53%）</div>
        <div style="font-size:.65rem; color:var(--text-secondary); margin-top:4px; line-height:1.5;">快速响应，不挑人<br>→ 对流量「数量」有强需求</div>
      </div>

      <div style="padding:12px 14px; border-left:3px solid #E1BC8B; background:rgba(225,188,139,.04); border-radius:0 8px 8px 0;">
        <div style="font-size:.72rem; font-weight:700; color:#E1BC8B;">佛系型（31%）</div>
        <div style="font-size:.65rem; color:var(--text-secondary); margin-top:4px; line-height:1.5;">看缘分，不关注详情<br>→ 对流量「量级」不敏感</div>
      </div>

      <div style="padding:12px 14px; border-left:3px solid #DE8784; background:rgba(222,135,132,.04); border-radius:0 8px 8px 0;">
        <div style="font-size:.72rem; font-weight:700; color:#DE8784;">挑剔型（16%）</div>
        <div style="font-size:.65rem; color:var(--text-secondary); margin-top:4px; line-height:1.5;">细看简历再决策<br>→ 对流量「质量」有要求</div>
      </div>
    </div>
  </div>
</div>
```

**使用时替换：**
- 坐标轴含义（X=成本/Y=流量 → 你的维度）
- 区域名称和条件标注
- 阈值点名称（PA/PR/PP/TD）
- 右侧画像卡片内容（聚类结果）
- 区域色块的位置和大小（根据数据比例调整rect坐标）

---

### 图表选择决策表（更新）

| 数据场景 | 推荐图表 | 组件编号 |
|---------|---------|---------|
| 多组数值对比 | 柱状图 | 61 |
| 时间序列/趋势 | 折线面积图 | 62 |
| 构成/占比 | 环形图 | 63 |
| AB实验对比 | 分组柱状图 | 64 |
| 阶段性下降/提升 | 面积折线图 | 65 |
| 多维画像 | 横向柱状图 | 66 |
| 两组反向趋势 | 双折线图 | 67 |
| 前后资源重分配 | 前后对比柱状图 | 68 |
| **阈值/区间决策** | **阈值区间图** | **69** |
| **双维度交叉/策略矩阵** | **矩阵分区图** | **70** |
| 行内迷你趋势 | SVG迷你图 | 60 |


---

### 71. 热力图 / 色阶矩阵（Heatmap）

适合：双维度交叉分析、分群转化率/复购率、相关性矩阵、ROI×达成交叉表

```html
<!-- 热力图：纯HTML表格+背景色深浅表示数值 -->
<div style="background:#fff; border-radius:14px; padding:28px 32px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <div style="font-size:.82rem; font-weight:700; color:var(--text-primary); text-align:center; margin-bottom:16px;">达成数量分组 × ROI 分组复购率热力图</div>

  <div style="display:flex; gap:16px; align-items:stretch;">
    <!-- 表格主体 -->
    <div style="flex:1; overflow:auto;">
      <table style="width:100%; border-collapse:separate; border-spacing:3px; font-size:.72rem; text-align:center;">
        <thead>
          <tr>
            <th style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;"></th>
            <th style="padding:8px 12px; font-weight:600; color:var(--text-primary);">0-0.5</th>
            <th style="padding:8px 12px; font-weight:600; color:var(--text-primary);">0.5-1</th>
            <th style="padding:8px 12px; font-weight:600; color:var(--text-primary);">1-2</th>
            <th style="padding:8px 12px; font-weight:600; color:var(--text-primary);">2+</th>
          </tr>
        </thead>
        <tbody>
          <!-- 行：每个td的background用rgba(67,140,128, 数值/最大值) -->
          <tr>
            <td style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;">1</td>
            <td style="padding:12px; background:rgba(67,140,128,.18); border-radius:4px; color:var(--text-primary); font-weight:600;">10.3%</td>
            <td style="padding:12px; background:rgba(67,140,128,.02); border-radius:4px; color:var(--text-primary);">0.0%</td>
            <td style="padding:12px; background:rgba(67,140,128,.02); border-radius:4px; color:var(--text-primary);">0.0%</td>
            <td style="padding:12px; background:rgba(67,140,128,.02); border-radius:4px; color:var(--text-primary);">0.0%</td>
          </tr>
          <tr>
            <td style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;">2-5</td>
            <td style="padding:12px; background:rgba(67,140,128,.34); border-radius:4px; color:var(--text-primary); font-weight:600;">19.1%</td>
            <td style="padding:12px; background:rgba(67,140,128,.17); border-radius:4px; color:var(--text-primary);">9.9%</td>
            <td style="padding:12px; background:rgba(67,140,128,.13); border-radius:4px; color:var(--text-primary);">7.7%</td>
            <td style="padding:12px; background:rgba(67,140,128,.40); border-radius:4px; color:var(--text-primary); font-weight:600;">22.2%</td>
          </tr>
          <tr>
            <td style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;">6-10</td>
            <td style="padding:12px; background:rgba(67,140,128,.42); border-radius:4px; color:var(--text-primary); font-weight:600;">23.2%</td>
            <td style="padding:12px; background:rgba(67,140,128,.58); border-radius:4px; color:#fff; font-weight:600;">31.3%</td>
            <td style="padding:12px; background:rgba(67,140,128,.32); border-radius:4px; color:var(--text-primary);">18.2%</td>
            <td style="padding:12px; background:rgba(67,140,128,.52); border-radius:4px; color:#fff; font-weight:600;">28.6%</td>
          </tr>
          <tr>
            <td style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;">11-20</td>
            <td style="padding:12px; background:rgba(67,140,128,.52); border-radius:4px; color:#fff; font-weight:600;">28.5%</td>
            <td style="padding:12px; background:rgba(67,140,128,.60); border-radius:4px; color:#fff; font-weight:600;">32.7%</td>
            <td style="padding:12px; background:rgba(67,140,128,.53); border-radius:4px; color:#fff; font-weight:600;">29.0%</td>
            <td style="padding:12px; background:rgba(67,140,128,.35); border-radius:4px; color:var(--text-primary);">19.4%</td>
          </tr>
          <tr>
            <td style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;">21-50</td>
            <td style="padding:12px; background:rgba(67,140,128,.48); border-radius:4px; color:#fff; font-weight:600;">26.6%</td>
            <td style="padding:12px; background:rgba(67,140,128,.58); border-radius:4px; color:#fff; font-weight:600;">32.0%</td>
            <td style="padding:12px; background:rgba(67,140,128,.63); border-radius:4px; color:#fff; font-weight:600;">34.5%</td>
            <td style="padding:12px; background:rgba(67,140,128,.65); border-radius:4px; color:#fff; font-weight:600;">35.8%</td>
          </tr>
          <tr>
            <td style="padding:8px 12px; font-weight:600; color:var(--text-secondary); text-align:left;">50+</td>
            <td style="padding:12px; background:rgba(67,140,128,.95); border-radius:4px; color:#fff; font-weight:700;">51.4%</td>
            <td style="padding:12px; background:rgba(67,140,128,.86); border-radius:4px; color:#fff; font-weight:700;">46.8%</td>
            <td style="padding:12px; background:rgba(67,140,128,.80); border-radius:4px; color:#fff; font-weight:700;">43.6%</td>
            <td style="padding:12px; background:rgba(67,140,128,.80); border-radius:4px; color:#fff; font-weight:700;">43.7%</td>
          </tr>
        </tbody>
      </table>
      <!-- 轴标签 -->
      <div style="text-align:center; font-size:.68rem; color:var(--text-secondary); margin-top:8px;">ROI 分组</div>
    </div>

    <!-- 右侧：色阶图例 -->
    <div style="width:24px; display:flex; flex-direction:column; align-items:center; gap:4px;">
      <span style="font-size:.58rem; color:var(--text-secondary);">50%</span>
      <div style="flex:1; width:16px; border-radius:8px; background:linear-gradient(to bottom, #438C80, rgba(67,140,128,.08));"></div>
      <span style="font-size:.58rem; color:var(--text-secondary);">0%</span>
    </div>
  </div>

  <div style="font-size:.62rem; color:var(--text-secondary); text-align:center; margin-top:12px;">单元格颜色越深表示复购率越高；单元格内仅展示复购率</div>
</div>
```

**使用时替换：**
- 行/列标签（Y轴分组/X轴分组）
- 每个 td 的数值和 background 的 rgba alpha 值（alpha ≈ 数值/最大值）
- 色阶颜色（默认用青绿 #438C80）
- 白色文字阈值：当 alpha > 0.5 时 td 文字用 `color:#fff`

**色阶计算规则：**
```
alpha = 数值 / 数据中最大值 × 0.95（避免纯黑）
当 alpha > 0.5 → 文字白色 + font-weight:600
当 alpha ≤ 0.5 → 文字黑色
```

---

### 72. 累积捕获曲线 / Lift Chart

适合：模型区分能力评估、AUC可视化、分群覆盖率分析、正样本捕获效率

```html
<!-- 累积捕获曲线：SVG绘制 -->
<div style="background:#fff; border-radius:14px; padding:28px 32px; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <div style="font-size:.82rem; font-weight:700; color:var(--text-primary); text-align:center; margin-bottom:20px;">正样本累积捕获曲线 · 模型区分能力</div>

  <svg viewBox="0 0 600 360" style="width:100%; height:auto;" xmlns="http://www.w3.org/2000/svg">
    <!-- 背景网格（极淡） -->
    <line x1="60" y1="60" x2="560" y2="60" stroke="rgba(0,0,0,.04)" stroke-width="1"/>
    <line x1="60" y1="135" x2="560" y2="135" stroke="rgba(0,0,0,.04)" stroke-width="1"/>
    <line x1="60" y1="210" x2="560" y2="210" stroke="rgba(0,0,0,.04)" stroke-width="1"/>
    <line x1="60" y1="285" x2="560" y2="285" stroke="rgba(0,0,0,.04)" stroke-width="1"/>

    <!-- 坐标轴 -->
    <line x1="60" y1="310" x2="560" y2="310" stroke="#ddd" stroke-width="1"/>
    <line x1="60" y1="35" x2="60" y2="310" stroke="#ddd" stroke-width="1"/>

    <!-- 45°对角线（随机基线） -->
    <line x1="60" y1="310" x2="560" y2="35" stroke="#ccc" stroke-width="1.5" stroke-dasharray="6,4"/>
    <text x="540" y="58" font-size="9" fill="#999">随机基线</text>

    <!-- 模型曲线下方填充 -->
    <path d="M60,310 L60,240 C110,205 160,155 210,120 C260,90 310,70 360,55 C410,45 460,40 510,37 L560,35 L560,310 Z" fill="rgba(67,140,128,.12)"/>

    <!-- 模型曲线 -->
    <path d="M60,240 C110,205 160,155 210,120 C260,90 310,70 360,55 C410,45 460,40 510,37 L560,35" fill="none" stroke="#438C80" stroke-width="2.5" stroke-linecap="round"/>

    <!-- 数据点 -->
    <circle cx="60" cy="240" r="4" fill="#438C80"/>
    <circle cx="116" cy="195" r="4" fill="#438C80"/>
    <circle cx="172" cy="150" r="4" fill="#438C80"/>
    <circle cx="228" cy="118" r="4" fill="#438C80"/>
    <circle cx="284" cy="92" r="4" fill="#438C80"/>
    <circle cx="340" cy="70" r="4" fill="#438C80"/>
    <circle cx="396" cy="55" r="4" fill="#438C80"/>
    <circle cx="452" cy="44" r="4" fill="#438C80"/>
    <circle cx="508" cy="38" r="4" fill="#438C80"/>
    <circle cx="560" cy="35" r="4" fill="#438C80"/>

    <!-- 关键标注：50%处竖虚线 -->
    <line x1="310" y1="35" x2="310" y2="310" stroke="#438C80" stroke-width="1.5" stroke-dasharray="4,3"/>
    <!-- 标注文字 -->
    <text x="315" y="48" font-size="9" font-weight="600" fill="#438C80">半数流量捕获 77% 正样本</text>
    <!-- 水平虚线到Y轴 -->
    <line x1="60" y1="70" x2="310" y2="70" stroke="#438C80" stroke-width="1" stroke-dasharray="3,3" opacity=".5"/>
    <!-- 标注数字 -->
    <text x="310" y="82" font-size="11" font-weight="700" fill="#438C80">77%</text>

    <!-- Y轴刻度 -->
    <text x="50" y="313" text-anchor="end" font-size="9" fill="#666">0%</text>
    <text x="50" y="213" text-anchor="end" font-size="9" fill="#666">25%</text>
    <text x="50" y="138" text-anchor="end" font-size="9" fill="#666">50%</text>
    <text x="50" y="63" text-anchor="end" font-size="9" fill="#666">75%</text>
    <text x="50" y="38" text-anchor="end" font-size="9" fill="#666">100%</text>

    <!-- X轴刻度 -->
    <text x="60" y="328" text-anchor="middle" font-size="9" fill="#666">10%</text>
    <text x="172" y="328" text-anchor="middle" font-size="9" fill="#666">30%</text>
    <text x="310" y="328" text-anchor="middle" font-size="9" fill="#666">50%</text>
    <text x="452" y="328" text-anchor="middle" font-size="9" fill="#666">80%</text>
    <text x="560" y="328" text-anchor="middle" font-size="9" fill="#666">100%</text>

    <!-- 轴标题 -->
    <text x="310" y="350" text-anchor="middle" font-size="10" fill="#666">样本百分比（按模型预测分排序）</text>
    <text x="18" y="175" font-size="10" fill="#666" writing-mode="tb" text-anchor="middle">累积捕获正样本%</text>
  </svg>
</div>
```

**使用时替换：**
- 曲线path的d属性（根据实际累积捕获数据点调整坐标）
- 数据点circle的cx/cy坐标
- 关键标注点位置和文字（如"半数流量捕获77%"）
- X/Y轴标题和含义

**坐标计算规则：**
```
X方向: 60px(0%) → 560px(100%), 总宽500px
Y方向: 310px(0%) → 35px(100%), 总高275px（注意Y轴反向）

数据点坐标:
  cx = 60 + (x百分比 × 500)
  cy = 310 - (y百分比 × 275)
```


---

### 73. 手绘虚线框卡片（Sketch Dashed Card）

适合：技能展示、多列并列概念、方法论要素、轻松风格分类。圆角虚线边框+手写风标签，不同颜色区分类别。

```html
<!-- 三列手绘虚线框 -->
<div style="display:grid; grid-template-columns:repeat(3, 1fr); gap:20px;">
  <!-- 卡片1：青绿 -->
  <div style="border:2px dashed #438C80; border-radius:16px; padding:24px 20px; position:relative;">
    <div style="position:absolute; top:-10px; left:16px; background:#fff; padding:0 8px; font-family:'Caveat',cursive; font-size:.85rem; color:#438C80;">Skill #1</div>
    <h4 style="font-size:.95rem; font-weight:700; color:var(--text-primary); margin-top:8px; margin-bottom:8px;">信息架构</h4>
    <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.6;">把混乱的信息整理成清晰结构</p>
  </div>
  <!-- 卡片2：暖金 -->
  <div style="border:2px dashed #E1BC8B; border-radius:16px; padding:24px 20px; position:relative;">
    <div style="position:absolute; top:-10px; left:16px; background:#fff; padding:0 8px; font-family:'Caveat',cursive; font-size:.85rem; color:#E1BC8B;">Skill #2</div>
    <h4 style="font-size:.95rem; font-weight:700; color:var(--text-primary); margin-top:8px; margin-bottom:8px;">视觉层次</h4>
    <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.6;">大小、颜色、间距引导视线</p>
  </div>
  <!-- 卡片3：玫瑰 -->
  <div style="border:2px dashed #DE8784; border-radius:16px; padding:24px 20px; position:relative;">
    <div style="position:absolute; top:-10px; left:16px; background:#fff; padding:0 8px; font-family:'Caveat',cursive; font-size:.85rem; color:#DE8784;">Skill #3</div>
    <h4 style="font-size:.95rem; font-weight:700; color:var(--text-primary); margin-top:8px; margin-bottom:8px;">微交互</h4>
    <p style="font-size:.78rem; color:var(--text-secondary); line-height:1.6;">细微动画让产品从可用变为可爱</p>
  </div>
</div>
```

**变体：**

```html
<!-- 变体A：2列大卡（更多描述空间） -->
<div style="display:grid; grid-template-columns:1fr 1fr; gap:20px;">
  <div style="border:2px dashed #438C80; border-radius:16px; padding:28px 24px; position:relative;">
    <div style="position:absolute; top:-10px; left:16px; background:#fff; padding:0 8px; font-family:'Caveat',cursive; font-size:.85rem; color:#438C80;">Step 1</div>
    <h4 style="font-size:1rem; font-weight:700; color:var(--text-primary); margin-top:8px; margin-bottom:10px;">标题内容</h4>
    <p style="font-size:.8rem; color:var(--text-secondary); line-height:1.7;">两行以上的描述文字，可以包含更多细节和数据支撑说明。</p>
  </div>
  <div style="border:2px dashed #E1BC8B; border-radius:16px; padding:28px 24px; position:relative;">
    <div style="position:absolute; top:-10px; left:16px; background:#fff; padding:0 8px; font-family:'Caveat',cursive; font-size:.85rem; color:#E1BC8B;">Step 2</div>
    <h4 style="font-size:1rem; font-weight:700; color:var(--text-primary); margin-top:8px; margin-bottom:10px;">标题内容</h4>
    <p style="font-size:.8rem; color:var(--text-secondary); line-height:1.7;">两行以上的描述文字，更丰富的信息承载。</p>
  </div>
</div>

<!-- 变体B：单个突出卡片（用于重点强调） -->
<div style="border:2.5px dashed #438C80; border-radius:20px; padding:32px 28px; position:relative; max-width:500px;">
  <div style="position:absolute; top:-12px; left:20px; background:#fff; padding:0 10px; font-family:'Caveat',cursive; font-size:.9rem; color:#438C80;">Key Point</div>
  <h4 style="font-size:1.1rem; font-weight:700; color:var(--text-primary); margin-top:6px; margin-bottom:10px;">核心观点标题</h4>
  <p style="font-size:.82rem; color:var(--text-secondary); line-height:1.7;">详细描述内容，可以是总结性观点或关键发现。手绘虚线框营造轻松感，适合团队分享场景。</p>
</div>
```

**使用规则：**
- 三色虚线区分不同类别/阶段/优先级
- 标签用 Caveat 手写字体（已在 Google Fonts 中引入）
- 标签文字可以是编号（Skill #1）、步骤（Step 1）、或自定义文字
- 适合轻松的团队分享场景，述职汇报中慎用（显得不够严肃）


---

### 74. 手绘标注文字（Text Highlighter · 多样式混合）

适合：正文中多处关键词需要不同形式的视觉标注（下划线波浪、圆圈圈注、方框框注）。比单一高亮更有手工感和层次感。

```html
<p style="font-size:.9rem; color:var(--text-primary); line-height:2.2; max-width:700px;">
  在设计系统中，<span style="border-bottom:2px solid #E1BC8B; padding-bottom:1px;">一致性比创新更重要</span>。每个组件都要证明价值——如果一个元素无法提升用户体验就该删掉。记住：
  <span style="display:inline-block; border:2px solid #DE8784; border-radius:50%; padding:2px 10px; margin:0 4px; position:relative;">
    少即是多
    <!-- 底部波浪线装饰 -->
    <svg style="position:absolute; bottom:-6px; left:10%; width:80%; height:6px;" viewBox="0 0 60 6" fill="none">
      <path d="M0,3 Q5,0 10,3 Q15,6 20,3 Q25,0 30,3 Q35,6 40,3 Q45,0 50,3 Q55,6 60,3" stroke="#DE8784" stroke-width="1.5" fill="none"/>
    </svg>
  </span>，这不是口号，是
  <span style="display:inline-block; border:1.5px solid #438C80; padding:1px 8px; margin:0 2px;">设计原则</span>。
</p>
```

**三种标注样式（可混合使用）：**

```html
<!-- 样式A：底部高亮线（最温和，适合一般强调） -->
<span style="border-bottom:2px solid #E1BC8B; padding-bottom:1px;">关键词</span>

<!-- 样式B：椭圆圈注（最强调，适合核心结论） -->
<span style="display:inline-block; border:2px solid #DE8784; border-radius:50%; padding:2px 10px; position:relative;">
  核心词
  <svg style="position:absolute; bottom:-6px; left:10%; width:80%; height:6px;" viewBox="0 0 60 6" fill="none">
    <path d="M0,3 Q5,0 10,3 Q15,6 20,3 Q25,0 30,3 Q35,6 40,3 Q45,0 50,3 Q55,6 60,3" stroke="#DE8784" stroke-width="1.5" fill="none"/>
  </svg>
</span>

<!-- 样式C：方框框注（中等强调，适合术语/定义） -->
<span style="display:inline-block; border:1.5px solid #438C80; padding:1px 8px;">术语</span>
```

**使用规则：**
- 一段文字中最多用3种标注，不超过4处
- 底部线用暖金（最弱）、方框用青绿（中等）、圆圈用玫瑰（最强）
- 适合团队分享和教程类PPT，述职汇报中慎用

---

### 75. 巨大引号居中（Centered Big Quote）

适合：金句页、核心理念、用户评价、章节总结。暖色背景+巨大引号+居中文字，营造沉稳有力量的引用感。

```html
<!-- 巨大引号居中 · 暖色背景版 -->
<div style="background:#f2ece4; border-radius:16px; padding:48px 40px; text-align:center; max-width:700px; margin:0 auto;">
  <div style="font-family:'Playfair Display',serif; font-size:1.4rem; font-weight:700; color:var(--text-primary); line-height:1.8; position:relative;">
    <span style="font-family:'Playfair Display',serif; font-size:1.4rem; color:var(--text-primary);">"</span>世界上最有力量的人，是那些能用简单的话说清楚复杂事情的人。<span style="font-family:'Playfair Display',serif; font-size:1.4rem; color:var(--text-primary);">"</span>
  </div>
  <div style="margin-top:20px; font-size:.78rem; color:var(--text-secondary);">— 理查德·费曼</div>
</div>
```

**变体：**

```html
<!-- 变体A：纯白背景+左侧大引号（更现代） -->
<div style="background:#fff; border-radius:16px; padding:40px 48px; max-width:700px; position:relative; box-shadow:0 2px 12px rgba(0,0,0,.04);">
  <div style="position:absolute; top:20px; left:28px; font-family:'Playfair Display',serif; font-size:4rem; color:#E1BC8B; opacity:.5; line-height:1;">"</div>
  <div style="padding-left:32px;">
    <div style="font-size:1.2rem; font-weight:700; color:var(--text-primary); line-height:1.8; font-style:italic;">
      数据不会说谎，但解读数据的人需要智慧和勇气。
    </div>
    <div style="margin-top:16px; font-size:.78rem; color:var(--text-secondary);">— 某资深数据分析师</div>
  </div>
</div>

<!-- 变体B：深色背景版（用于深色页面） -->
<div style="background:rgba(1,0,5,.85); border-radius:16px; padding:48px 40px; text-align:center; max-width:700px; margin:0 auto;">
  <div style="font-family:'Playfair Display',serif; font-size:1.4rem; font-weight:700; color:#f1f5f9; line-height:1.8;">
    "Less is more, but better is best."
  </div>
  <div style="margin-top:20px; font-size:.78rem; color:rgba(255,255,255,.5);">— Dieter Rams</div>
</div>

<!-- 变体C：三色装饰线版（带品牌感） -->
<div style="background:#faf9f8; border-radius:16px; padding:48px 40px; text-align:center; max-width:700px; margin:0 auto; position:relative;">
  <!-- 顶部三色装饰线 -->
  <div style="position:absolute; top:0; left:50%; transform:translateX(-50%); display:flex; gap:4px;">
    <div style="width:24px; height:3px; background:#438C80; border-radius:0 0 2px 2px;"></div>
    <div style="width:24px; height:3px; background:#E1BC8B; border-radius:0 0 2px 2px;"></div>
    <div style="width:24px; height:3px; background:#DE8784; border-radius:0 0 2px 2px;"></div>
  </div>
  <div style="font-family:'Playfair Display',serif; font-size:1.3rem; font-weight:700; color:var(--text-primary); line-height:1.8; margin-top:8px;">
    "用最少的元素，传达最强的信息。"
  </div>
  <div style="margin-top:16px; font-size:.78rem; color:var(--text-secondary);">— 设计原则</div>
</div>
```

**使用规则：**
- 暖色背景版（#f2ece4）适合轻松分享场景
- 白色版适合述职汇报中的金句页
- 深色版仅用于深色页面（封面/结尾）
- 一份PPT中金句页最多2页，不要滥用


---

### 76. Do/Don't 表格对比（Checklist Table）

适合：规范说明、最佳实践清单、设计准则、代码规范。深色表头+白色行+图标式✓/✗标记，简洁清晰。

```html
<div style="border-radius:12px; overflow:hidden; box-shadow:0 2px 12px rgba(0,0,0,.04); max-width:700px;">
  <table style="width:100%; border-collapse:collapse; font-size:.82rem;">
    <thead>
      <tr style="background:#1a1a1a; color:#fff;">
        <th style="padding:12px 20px; text-align:left; font-weight:600;">实践</th>
        <th style="padding:12px 16px; text-align:center; font-weight:600; width:60px;">DON'T</th>
        <th style="padding:12px 16px; text-align:center; font-weight:600; width:60px;">DO</th>
      </tr>
    </thead>
    <tbody>
      <tr style="border-bottom:1px solid #f0eeec;">
        <td style="padding:14px 20px; color:var(--text-primary);">使用默认引用样式</td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:50%;background:rgba(222,135,132,.12);color:#DE8784;font-size:.7rem;font-weight:700;">⊘</span></td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:6px;background:rgba(67,140,128,.12);color:#438C80;font-size:.75rem;font-weight:700;">✓</span></td>
      </tr>
      <tr style="border-bottom:1px solid #f0eeec;">
        <td style="padding:14px 20px; color:var(--text-primary);">一致的视觉语言</td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:50%;background:rgba(222,135,132,.12);color:#DE8784;font-size:.7rem;font-weight:700;">⊘</span></td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:6px;background:rgba(67,140,128,.12);color:#438C80;font-size:.75rem;font-weight:700;">✓</span></td>
      </tr>
      <tr style="border-bottom:1px solid #f0eeec;">
        <td style="padding:14px 20px; color:var(--text-primary);">真实内容Demo</td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:50%;background:rgba(222,135,132,.12);color:#DE8784;font-size:.7rem;font-weight:700;">⊘</span></td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:6px;background:rgba(67,140,128,.12);color:#438C80;font-size:.75rem;font-weight:700;">✓</span></td>
      </tr>
      <tr>
        <td style="padding:14px 20px; color:var(--text-primary);">克制使用动效</td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:50%;background:rgba(222,135,132,.12);color:#DE8784;font-size:.7rem;font-weight:700;">⊘</span></td>
        <td style="padding:14px 16px; text-align:center;"><span style="display:inline-flex;align-items:center;justify-content:center;width:24px;height:24px;border-radius:6px;background:rgba(67,140,128,.12);color:#438C80;font-size:.75rem;font-weight:700;">✓</span></td>
      </tr>
    </tbody>
  </table>
</div>
```

---

### 77. Do/Don't 印章边框（Stamp Border）

适合：设计规范、正反对比、Avoid vs Prefer。左右分栏各带彩色实线边框+顶部标签打断边框（印章效果）。

```html
<div style="display:grid; grid-template-columns:1fr 1fr; gap:24px; max-width:800px;">
  <!-- AVOID 左侧 -->
  <div style="border:2px solid #DE8784; border-radius:12px; padding:28px 24px; position:relative;">
    <div style="position:absolute; top:-11px; left:50%; transform:translateX(-50%); background:#fff; padding:0 12px; font-family:'JetBrains Mono',monospace; font-size:.7rem; font-weight:700; color:#DE8784; letter-spacing:3px;">AVOID</div>
    <div style="display:flex; flex-direction:column; gap:12px; margin-top:8px;">
      <div style="display:flex; align-items:flex-start; gap:8px;">
        <span style="color:#DE8784; font-weight:700; font-size:.8rem;">✕</span>
        <span style="font-size:.8rem; color:var(--text-primary);">过度设计、过多装饰</span>
      </div>
      <div style="display:flex; align-items:flex-start; gap:8px;">
        <span style="color:#DE8784; font-weight:700; font-size:.8rem;">✕</span>
        <span style="font-size:.8rem; color:var(--text-primary);">不同section不同风格</span>
      </div>
      <div style="display:flex; align-items:flex-start; gap:8px;">
        <span style="color:#DE8784; font-weight:700; font-size:.8rem;">✕</span>
        <span style="font-size:.8rem; color:var(--text-primary);">用AI生成的stock风图片</span>
      </div>
    </div>
  </div>
  <!-- PREFER 右侧 -->
  <div style="border:2px solid #438C80; border-radius:12px; padding:28px 24px; position:relative;">
    <div style="position:absolute; top:-11px; left:50%; transform:translateX(-50%); background:#fff; padding:0 12px; font-family:'JetBrains Mono',monospace; font-size:.7rem; font-weight:700; color:#438C80; letter-spacing:3px;">PREFER</div>
    <div style="display:flex; flex-direction:column; gap:12px; margin-top:8px;">
      <div style="display:flex; align-items:flex-start; gap:8px;">
        <span style="color:#438C80; font-weight:700; font-size:.8rem;">◆</span>
        <span style="font-size:.8rem; color:var(--text-primary);">简洁、留白、有呼吸感</span>
      </div>
      <div style="display:flex; align-items:flex-start; gap:8px;">
        <span style="color:#438C80; font-weight:700; font-size:.8rem;">◆</span>
        <span style="font-size:.8rem; color:var(--text-primary);">统一视觉语言贯穿全页</span>
      </div>
      <div style="display:flex; align-items:flex-start; gap:8px;">
        <span style="color:#438C80; font-weight:700; font-size:.8rem;">◆</span>
        <span style="font-size:.8rem; color:var(--text-primary);">高清真实图片</span>
      </div>
    </div>
  </div>
</div>
```

---

### 78. 杂志对比表（Editorial VS Table）

适合：两种方案/模式/产品对比。左侧大VS装饰+右侧编号行对比，杂志排版感。

```html
<div style="display:flex; gap:32px; align-items:center; max-width:850px;">
  <!-- 左侧：VS标题区 -->
  <div style="min-width:160px;">
    <div style="font-family:'Playfair Display',serif; font-size:3.5rem; font-weight:900; color:#E1BC8B; opacity:.5; line-height:1;">VS</div>
    <div style="font-family:'JetBrains Mono',monospace; font-size:.68rem; color:var(--text-secondary); margin-top:4px;">04</div>
    <div style="font-size:1rem; font-weight:900; color:var(--text-primary); margin-top:8px;">传统开发 vs AI开发</div>
    <div style="font-size:.72rem; color:var(--text-secondary); margin-top:4px;">两种范式的核心差异</div>
  </div>
  <!-- 右侧：对比行 -->
  <div style="flex:1; display:flex; flex-direction:column; gap:0;">
    <!-- 行1 -->
    <div style="display:flex; align-items:center; padding:16px 0; border-bottom:1px solid #f0eeec;">
      <div style="font-family:'Playfair Display',serif; font-size:1.3rem; font-weight:900; color:#438C80; min-width:40px;">01</div>
      <div style="flex:1; padding:0 16px;">
        <div style="font-size:.65rem; color:var(--text-secondary);">启动成本</div>
        <div style="font-size:.88rem; font-weight:700; color:var(--text-primary);">数周学习+环境配置</div>
      </div>
      <div style="flex:1; padding:0 16px;">
        <div style="font-size:.65rem; color:var(--text-secondary);">AI 开发</div>
        <div style="font-size:.88rem; font-weight:700; color:var(--text-primary);">一句话描述即开始</div>
      </div>
    </div>
    <!-- 行2 -->
    <div style="display:flex; align-items:center; padding:16px 0; border-bottom:1px solid #f0eeec;">
      <div style="font-family:'Playfair Display',serif; font-size:1.3rem; font-weight:900; color:#438C80; min-width:40px;">02</div>
      <div style="flex:1; padding:0 16px;">
        <div style="font-size:.65rem; color:var(--text-secondary);">迭代速度</div>
        <div style="font-size:.88rem; font-weight:700; color:var(--text-primary);">天/周级别</div>
      </div>
      <div style="flex:1; padding:0 16px;">
        <div style="font-size:.65rem; color:var(--text-secondary);">AI 开发</div>
        <div style="font-size:.88rem; font-weight:700; color:var(--text-primary);">分钟/小时级别</div>
      </div>
    </div>
    <!-- 行3 -->
    <div style="display:flex; align-items:center; padding:16px 0;">
      <div style="font-family:'Playfair Display',serif; font-size:1.3rem; font-weight:900; color:#438C80; min-width:40px;">03</div>
      <div style="flex:1; padding:0 16px;">
        <div style="font-size:.65rem; color:var(--text-secondary);">技能门槛</div>
        <div style="font-size:.88rem; font-weight:700; color:var(--text-primary);">需要专业编程知识</div>
      </div>
      <div style="flex:1; padding:0 16px;">
        <div style="font-size:.65rem; color:var(--text-secondary);">AI 开发</div>
        <div style="font-size:.88rem; font-weight:700; color:var(--text-primary);">会描述需求即可</div>
      </div>
    </div>
  </div>
</div>
```

---

### 79. 横向时间线（Horizontal Timeline）

适合：阶段展示、项目里程碑、成长路径、迭代阶段。横向排列各阶段，手写风标签+多色标题。

```html
<div style="display:grid; grid-template-columns:repeat(4, 1fr); gap:24px; max-width:850px;">
  <!-- Phase 1 -->
  <div>
    <div style="font-family:'Caveat',cursive; font-size:.82rem; color:var(--text-secondary); margin-bottom:6px;">Phase 1</div>
    <div style="font-size:1.05rem; font-weight:900; color:#DE8784; margin-bottom:8px;">探索期</div>
    <div style="font-size:.75rem; color:var(--text-secondary); line-height:1.6;">大量阅读、观察、收集灵感</div>
  </div>
  <!-- Phase 2 -->
  <div>
    <div style="font-family:'Caveat',cursive; font-size:.82rem; color:var(--text-secondary); margin-bottom:6px;">Phase 2</div>
    <div style="font-size:1.05rem; font-weight:900; color:#438C80; margin-bottom:8px;">聚焦期</div>
    <div style="font-size:.75rem; color:var(--text-secondary); line-height:1.6;">确定方向，深入钻研一个领域</div>
  </div>
  <!-- Phase 3 -->
  <div>
    <div style="font-family:'Caveat',cursive; font-size:.82rem; color:var(--text-secondary); margin-bottom:6px;">Phase 3</div>
    <div style="font-size:1.05rem; font-weight:900; color:#E1BC8B; margin-bottom:8px;">输出期</div>
    <div style="font-size:.75rem; color:var(--text-secondary); line-height:1.6;">把积累转化为可见的作品</div>
  </div>
  <!-- Phase 4 -->
  <div>
    <div style="font-family:'Caveat',cursive; font-size:.82rem; color:var(--text-secondary); margin-bottom:6px;">Phase 4</div>
    <div style="font-size:1.05rem; font-weight:900; color:var(--text-primary); margin-bottom:8px;">扩展期</div>
    <div style="font-size:.75rem; color:var(--text-secondary); line-height:1.6;">建立系统，影响更多人</div>
  </div>
</div>
```

**变体：带连接线版**

```html
<div style="position:relative; max-width:850px;">
  <!-- 连接线 -->
  <div style="position:absolute; top:32px; left:8%; right:8%; height:2px; background:linear-gradient(to right, #DE8784, #438C80, #E1BC8B, #010005); border-radius:1px;"></div>
  <!-- 节点 -->
  <div style="display:grid; grid-template-columns:repeat(4, 1fr); gap:24px; position:relative; z-index:1;">
    <div style="text-align:center;">
      <div style="width:12px; height:12px; background:#DE8784; border-radius:50%; border:3px solid #fff; box-shadow:0 0 0 2px #DE8784; margin:26px auto 12px;"></div>
      <div style="font-family:'Caveat',cursive; font-size:.78rem; color:var(--text-secondary);">Phase 1</div>
      <div style="font-size:.92rem; font-weight:900; color:#DE8784; margin:4px 0;">探索期</div>
      <div style="font-size:.7rem; color:var(--text-secondary); line-height:1.5;">大量阅读<br>收集灵感</div>
    </div>
    <div style="text-align:center;">
      <div style="width:12px; height:12px; background:#438C80; border-radius:50%; border:3px solid #fff; box-shadow:0 0 0 2px #438C80; margin:26px auto 12px;"></div>
      <div style="font-family:'Caveat',cursive; font-size:.78rem; color:var(--text-secondary);">Phase 2</div>
      <div style="font-size:.92rem; font-weight:900; color:#438C80; margin:4px 0;">聚焦期</div>
      <div style="font-size:.7rem; color:var(--text-secondary); line-height:1.5;">深入钻研<br>一个领域</div>
    </div>
    <div style="text-align:center;">
      <div style="width:12px; height:12px; background:#E1BC8B; border-radius:50%; border:3px solid #fff; box-shadow:0 0 0 2px #E1BC8B; margin:26px auto 12px;"></div>
      <div style="font-family:'Caveat',cursive; font-size:.78rem; color:var(--text-secondary);">Phase 3</div>
      <div style="font-size:.92rem; font-weight:900; color:#E1BC8B; margin:4px 0;">输出期</div>
      <div style="font-size:.7rem; color:var(--text-secondary); line-height:1.5;">积累转化<br>可见作品</div>
    </div>
    <div style="text-align:center;">
      <div style="width:12px; height:12px; background:#010005; border-radius:50%; border:3px solid #fff; box-shadow:0 0 0 2px #010005; margin:26px auto 12px;"></div>
      <div style="font-family:'Caveat',cursive; font-size:.78rem; color:var(--text-secondary);">Phase 4</div>
      <div style="font-size:.92rem; font-weight:900; color:var(--text-primary); margin:4px 0;">扩展期</div>
      <div style="font-size:.7rem; color:var(--text-secondary); line-height:1.5;">建立系统<br>影响更多人</div>
    </div>
  </div>
</div>
```
