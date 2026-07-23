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
