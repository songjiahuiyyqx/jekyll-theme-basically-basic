---
layout: page
title: svg笔记
excerpt_separator: "<!--more-->"
categories:
      - SVG笔记
---
### svg动态图标
<!--more-->
### 原代码
```
<div class="draw-box">
	<div class="typewriter-effect">TIME TO DRINK COFFEE?</div>
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
    <defs>
      <mask id="rippleMask">
        <path
              class="ripple"
              d="M7.06,99.17c-.65-5.6,12.32,8.32,20.19-1.53C39,83,51.84,90.68,55.48,90.08c8.16-1.35,10-11.68,19-17s20.87,7.17,28.7-3.86c5.1-7.18,9.56-9.6,13.77-11.17,9.51-3.54,19.25,12.07,23.29.38,7-20.43,26.91-6.41,31.46-20,3-9,14.37-14.93,29.66-10C217.15,33.48,222-5.11,236.72,3.69c19.63,11.74,40,74.88,50.33,104.82,29.8,86-61.63,121.55-82.21,130.28C148,262.91,91.31,274,53.8,208.12,53.8,208.12,8.23,109.3,7.06,99.17Z"
              fill="white"
              />
      </mask>
      <filter id="noise">
        <feTurbulence
                      baseFrequency="0.01 0.1"
                      result="WAVE"
                      numOctaves="1"
                      id="turbulence"
                      />
        <feDisplacementMap
                           in="SourceGraphic"
                           in2="WAVE"
                           scale="1.2"
                           ></feDisplacementMap>
      </filter>
    </defs>

<!-- Coffee cup -->
		<path
			class="coffeeColor"
			mask="url(#rippleMask)"
			d="M18.26,30.74c.83-.89,3.88-1.18,5.38.65,3.22,4,7.52,1.41,9.24-.17,3.74-3.42,6.53,4.75,11.75,1.16,3.55-2.45,5.34.12,8.95.33a9.38,9.38,0,0,0,6-1.68c4-2.5,6.35,3.33,10,2.88s4.91-3.5,7.79-2.77c0,0,0,1.82,0,2.49a14.07,14.07,0,0,1,11,.95C94.63,38,94,53.64,79.66,59.23l-5.33,2C73.13,66.54,69.6,73,66,73.68l-16.55,0H29.87c-10.81-1.87-11.58-33.19-11.6-44.1Zm67.49,8.38c-3.42-2.67-8.41-.38-8.46.49-.55,8.8-1.73,13.94-1.77,15.13,0,.45,7.28-1.55,10-5.28C87.39,46.77,89.15,41.79,85.75,39.12Z"
		/>
		<g mask="url(#rippleMask)" filter="url(#noise)">
			<path
				class="steamColor"
				d="M43,19.66c-.34.41.27-2.76-1.14-4.48-1.54-1.9-2.1-2.26-3-4-1.56-3.13,1.28-5.87,1.22-4.37C40,11,41.34,12.74,41.82,13.34a7.13,7.13,0,0,1,1.74,3A4.07,4.07,0,0,1,43,19.66Z"
			/>
			<path
				class="steamColor"
				d="M49,18.84c-.15.17-.25-.63.2-1.62,1.93-4.27-2.94-7.18-3-9.67-.08-3.48,2.58-4.64,2-3.76-2.8,4.68,1.66,6.79,2.42,9.85C51.18,15.53,49.89,17.91,49,18.84Z"
			/>
			<path
				class="steamColor"
				d="M55.26,19.67c-.16.13-.3-.92.23-1.8,3.3-5.52-.66-4.67.14-9.24.56-3.26,3.34-4,2.72-3.27C55.09,9.42,58,11.74,57.54,15A8.66,8.66,0,0,1,55.26,19.67Z"
			/>
		</g>

<!-- Stroke -->
		<path
			class="stroke"
			stroke-dasharray="267.4718933105469"
			stroke-dashoffset="267.4718933105469"
			d="M88.35,34.6a14,14,0,0,0-11-1c0-1.52.14-7.74.16-8,.08-1.52-1.8-1.52-1.8-1.52l-25.35,0H45.65l-25.35.05s-1.88,0-1.79,1.52S17.26,71.33,30.07,73.55h36c3.63-.64,7.14-7.11,8.34-12.41l5.31-2C94,53.59,94.62,38,88.35,34.6ZM85.49,49.42c-2.66,3.72-9.92,5.72-9.91,5.27,0-1.19,1.21-6.31,1.76-15.08,0-.87,5-3.16,8.43-.49S87.41,46.74,85.49,49.42Z"
		/>
	</svg>
</div>
```
#### 在这静态图标基础上，我添加如下命令
```
<animate attributeName="x" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="300" to="0"/>
		<animate attributeName="y" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="100" to="0"/>
		<animate attributeName="width" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="300" to="800"/>
		<animate attributeName="height" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="100" to="300"/>
		<animate attributeType="CSS"  from="1" to="0" dur="6s" repeatCount="indefinite">
```
- 这是我们刚开始学svg的内容

### 效果如下：
<div><div class="draw-box">
	<div class="typewriter-effect">TIME TO DRINK COFFEE?</div>
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
    <defs>
      <mask id="rippleMask">
        <path
              class="ripple"
              d="M7.06,99.17c-.65-5.6,12.32,8.32,20.19-1.53C39,83,51.84,90.68,55.48,90.08c8.16-1.35,10-11.68,19-17s20.87,7.17,28.7-3.86c5.1-7.18,9.56-9.6,13.77-11.17,9.51-3.54,19.25,12.07,23.29.38,7-20.43,26.91-6.41,31.46-20,3-9,14.37-14.93,29.66-10C217.15,33.48,222-5.11,236.72,3.69c19.63,11.74,40,74.88,50.33,104.82,29.8,86-61.63,121.55-82.21,130.28C148,262.91,91.31,274,53.8,208.12,53.8,208.12,8.23,109.3,7.06,99.17Z"
              fill="white"
              />
      </mask>
      <filter id="noise">
        <feTurbulence
                      baseFrequency="0.01 0.1"
                      result="WAVE"
                      numOctaves="1"
                      id="turbulence"
                      />
        <feDisplacementMap
                           in="SourceGraphic"
                           in2="WAVE"
                           scale="1.2"
                           ></feDisplacementMap>
      </filter>
    </defs>
		<path
			class="coffeeColor"
			mask="url(#rippleMask)"
			d="M18.26,30.74c.83-.89,3.88-1.18,5.38.65,3.22,4,7.52,1.41,9.24-.17,3.74-3.42,6.53,4.75,11.75,1.16,3.55-2.45,5.34.12,8.95.33a9.38,9.38,0,0,0,6-1.68c4-2.5,6.35,3.33,10,2.88s4.91-3.5,7.79-2.77c0,0,0,1.82,0,2.49a14.07,14.07,0,0,1,11,.95C94.63,38,94,53.64,79.66,59.23l-5.33,2C73.13,66.54,69.6,73,66,73.68l-16.55,0H29.87c-10.81-1.87-11.58-33.19-11.6-44.1Zm67.49,8.38c-3.42-2.67-8.41-.38-8.46.49-.55,8.8-1.73,13.94-1.77,15.13,0,.45,7.28-1.55,10-5.28C87.39,46.77,89.15,41.79,85.75,39.12Z"
		/>
		<g mask="url(#rippleMask)" filter="url(#noise)">
			<path
				class="steamColor"
				d="M43,19.66c-.34.41.27-2.76-1.14-4.48-1.54-1.9-2.1-2.26-3-4-1.56-3.13,1.28-5.87,1.22-4.37C40,11,41.34,12.74,41.82,13.34a7.13,7.13,0,0,1,1.74,3A4.07,4.07,0,0,1,43,19.66Z"
			/>
			<path
				class="steamColor"
				d="M49,18.84c-.15.17-.25-.63.2-1.62,1.93-4.27-2.94-7.18-3-9.67-.08-3.48,2.58-4.64,2-3.76-2.8,4.68,1.66,6.79,2.42,9.85C51.18,15.53,49.89,17.91,49,18.84Z"
			/>
			<path
				class="steamColor"
				d="M55.26,19.67c-.16.13-.3-.92.23-1.8,3.3-5.52-.66-4.67.14-9.24.56-3.26,3.34-4,2.72-3.27C55.09,9.42,58,11.74,57.54,15A8.66,8.66,0,0,1,55.26,19.67Z"
			/>
		</g>
		<path
			class="stroke"
			stroke-dasharray="267.4718933105469"
			stroke-dashoffset="267.4718933105469"
			d="M88.35,34.6a14,14,0,0,0-11-1c0-1.52.14-7.74.16-8,.08-1.52-1.8-1.52-1.8-1.52l-25.35,0H45.65l-25.35.05s-1.88,0-1.79,1.52S17.26,71.33,30.07,73.55h36c3.63-.64,7.14-7.11,8.34-12.41l5.31-2C94,53.59,94.62,38,88.35,34.6ZM85.49,49.42c-2.66,3.72-9.92,5.72-9.91,5.27,0-1.19,1.21-6.31,1.76-15.08,0-.87,5-3.16,8.43-.49S87.41,46.74,85.49,49.42Z"
		/>
		<animate attributeName="x" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="300" to="0"/>
		<animate attributeName="y" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="100" to="0"/>
		<animate attributeName="width" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="300" to="800"/>
		<animate attributeName="height" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="100" to="300"/>
		<animate attributeType="CSS"  from="1" to="0" dur="6s" repeatCount="indefinite">
			body {
			background-color: #232f3a;
  height: 100vh;
  display: grid;
  place-items: center;
  .draw-box {
    overflow: hidden;
    position: relative;
    margin-top: 60px;
    width: 335px;
    .typewriter-effect {
      overflow: hidden;
      animation: typingEffect 1.6s steps(22) forwards,
        blinkTextCursor 1s infinite;
      width: 0;
      color: #e8e8e8;
      height: 30px;
      font-size: 34px;
      white-space: nowrap;
      vertical-align: middle;
      line-height: 0.9;
      font-family: 'Barlow Semi Condensed', sans-serif;
    }
    @keyframes typingEffect {
      from {
        width: 0;
      }
      to {
        width: 98%;
      }
    }
    @keyframes blinkTextCursor {
      from {
        border-right: 3px solid #f8f8f8;
      }
      to {
        border-right: transparent;
      }
    }
    svg {
      width: 93%;
      margin-top: 10px;
      .stroke {
        fill: none;
        stroke: #e8e8e8;
        stroke-width: 0.8;
      }
      .coffeeColor {
        fill: #b59440;
        // fill: #6d6550; //Coffee color
      }
      .steamColor {
        fill: #ddd;
      }
      .ripple {
        transform: translate3d(-30%, 100%, 0);
      }
    }
  }
}
		</svg></div>

---

#### 这是我的动画尝试效果

---

#### 希望我的svg笔记过程，可以帮助你了解svg		