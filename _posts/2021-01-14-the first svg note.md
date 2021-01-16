---
layout: page
title: svg笔记
excerpt_separator: "<!--more-->"
categories:
      - svg笔记
---
### 网页设计就业
<!--more-->
### 原代码
```
<svg t="1610788423458" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="7048" width="200" height="200"><path d="M448 160v160c0 106.032 85.968 192 192 192s192 85.968 192 192v96a32 32 0 0 1-32 32H32c-17.696 0-32-14.32-32-32V160h448z" fill="#469FCC" p-id="7049"></path><path d="M32 960h96v-128h64v128h448v-128h64v128h128a128 128 0 0 0 128-128 31.984 31.984 0 1 1 64 0c0 106.032-85.968 192-192 192H32c-17.696 0-32-14.32-32-32s14.304-32 32-32z" fill="#DAE2E5" p-id="7050"></path><path d="M640 832h64v32h-64zM128 832h64v32H128z" opacity=".1" p-id="7051"></path><path d="M832 704v96a32 32 0 0 1-32 32H32c-17.696 0-32-14.32-32-32v-96h832z" opacity=".15" p-id="7052"></path><path d="M288 288c0-17.68 14.304-32 32-32h128v64h-128c-17.696 0-32-14.32-32-32zM320 384h139.152a191.84 191.84 0 0 0 38.032 64H320c-17.696 0-32-14.32-32-32s14.304-32 32-32z" opacity=".15" p-id="7053"></path><path d="M0 0h448a32 32 0 0 1 32 32v96a32 32 0 0 1-32 32H0V0z" fill="#434854" p-id="7054"></path><path d="M0 160h448v32H0z" opacity=".15" p-id="7055"></path></svg>
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
<div><svg t="1610788423458" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="7048" width="200" height="200"><path d="M448 160v160c0 106.032 85.968 192 192 192s192 85.968 192 192v96a32 32 0 0 1-32 32H32c-17.696 0-32-14.32-32-32V160h448z" fill="#469FCC" p-id="7049"></path><path d="M32 960h96v-128h64v128h448v-128h64v128h128a128 128 0 0 0 128-128 31.984 31.984 0 1 1 64 0c0 106.032-85.968 192-192 192H32c-17.696 0-32-14.32-32-32s14.304-32 32-32z" fill="#DAE2E5" p-id="7050"></path><path d="M640 832h64v32h-64zM128 832h64v32H128z" opacity=".1" p-id="7051"></path><path d="M832 704v96a32 32 0 0 1-32 32H32c-17.696 0-32-14.32-32-32v-96h832z" opacity=".15" p-id="7052"></path><path d="M288 288c0-17.68 14.304-32 32-32h128v64h-128c-17.696 0-32-14.32-32-32zM320 384h139.152a191.84 191.84 0 0 0 38.032 64H320c-17.696 0-32-14.32-32-32s14.304-32 32-32z" opacity=".15" p-id="7053"></path><path d="M0 0h448a32 32 0 0 1 32 32v96a32 32 0 0 1-32 32H0V0z" fill="#434854" p-id="7054"></path><path d="M0 160h448v32H0z" opacity=".15" p-id="7055"></path></svg>
		<animate attributeName="x" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="300" to="0"/>
		<animate attributeName="y" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="100" to="0"/>
		<animate attributeName="width" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="300" to="800"/>
		<animate attributeName="height" attributeType="XML" begin="0s" dur="5s" fill="freeze" from="100" to="300"/>
		<animate attributeType="CSS"  from="1" to="0" dur="6s" repeatCount="indefinite">
		</svg></div>