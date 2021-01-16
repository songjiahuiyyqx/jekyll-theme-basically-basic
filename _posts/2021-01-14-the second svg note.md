---
layout: page
title: svg笔记
excerpt_separator: "<!--more-->"
categories:
      - SVG笔记
---
### svg动态图标
<!--more-->

### 效果如下：

### SVG 渐变
- 渐变是一种从一种颜色到另一种颜色的平滑过渡。另外，可以把多个颜色的过渡应用到同一个元素上。
  - 在 SVG 中，有两种主要的渐变类型：
    - 线性渐变
    - 放射性渐变
---
<svg>
    <defs>
        <linearGradient id="greenGradient">
            <stop offset="0%" stop-color="#b2ed9d" />
            <stop offset="50%" stop-color="#00bfff" />
            <stop offset="100%" stop-color="#569b3d" />
        </linearGradient>
    </defs>
    <rect width="600" height="100" fill= "url(#greenGradient)" />
</svg>
- 代码如下

```
<svg>
    <defs>
        <linearGradient id="greenGradient">
            <stop offset="0" stop-color="#b2ed9d" />
            <stop offset="50" stop-color="#00bfff" />
            <stop offset="100%" stop-color="#569b3d" />
        </linearGradient>
    </defs>
    <rect width="600" height="100" fill= "url(#greenGradient)" />
</svg>
```
- 在这段代码中，渐变的元素都写在了```<def>```中，而```<stop>```元素代表了在渐变的颜色和它们的位置。
- ```<linearGradient>```和```<radialGradient>```允许我们指定渐变的颜色和坐标。

<svg width="500" height="500" color="green">
  <rect id="shadiao" x="20" y="20" width="100" height="100" fill="url(#yg)">    
    <animate
                   
                    attributeName="x"
                    attributeType="XML"
                    values="20;300;20"
                    begin="0s"
                    dur="2s"
                    repeatCount="indefinite"
                    />
</rect>
<defs>
    <linearGradient id="yg">
        <stop offset="0%" stop-color="#1e90ff">
          <animate attributeName="stop-color" values="#1e90ff; #00ff7f" dur="2s" repeatCount="indefinite" />
        </stop>
        <stop offset="100%" stop-color="#00ff7f">
          <animate attributeName="stop-color" values="#00ff7f; #1e90ff" dur="2s" repeatCount="indefinite" />
        </stop>
    </linearGradient>
</defs>
</svg>

#### 这是来回走的渐变方块

---

#### 这是我的动画尝试效果

---

#### 希望我的svg笔记过程，可以帮助你了解svg		