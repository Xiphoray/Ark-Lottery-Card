# 🎫 Ark Lottery Card (阿卡纳幸运签)

一个基于原生 HTML5/CSS3 打造的**横屏沉浸式抽奖交互组件**。采用高度仿真的票签设计与平滑的贝塞尔曲线动画，为 Web 应用提供极致的开奖仪式感。

## 📖 项目简介

`Ark Lottery Card` 模拟了线下抽签的互动场景。用户需要在流动的幸运墙中选择两枚幸运笺，系统将通过动态算法决定最终的中奖结果。本项目完全使用**原生技术栈**开发，无需任何第三方框架（如 React/Vue），轻量且易于集成。

## ✨ 核心特性

* **🎨 拟物化设计**：利用 CSS 线性渐变与 `clip-path` 模拟真实的纸张防伪纹理与锯齿边框。
* **📱 移动端优化**：内置强制横屏检测遮罩，确保在不同尺寸手机上均有完美的视觉呈现。
* **🎭 沉浸式交互**：
* **动态响应**：实时计算剩余可选签数。
* **视差反馈**：未选中签位在开奖时会自动降权淡出，突出显示中奖者。


* **⚙️ 灵活配置**：通过 CSS Variables (`:root`) 可快速调整签位的宽度、高度及间距。
* **⚡ 极致性能**：纯 CSS 驱动硬件加速动画，GPU 压力小，响应极速。

## 🛠️ 技术实现

### 1. 布局算法 (Geometric Layout)

项目采用了一种特殊的“中心咬合”布局。上下两排签位通过 `transform: rotate()` 以不同的弧度向中心线延伸，利用负边距实现交错美感。

### 2. 抽奖逻辑 (Logic Flow)

```javascript
// 核心逻辑简述
const winnerIndex = Math.random() > 0.5 ? 0 : 1; // 1/2 概率算法
const finalPrize = prizePool[Math.floor(Math.random() * prizePool.length)]; // 随机奖池

```

## 🚀 快速开始

### 集成到项目

由于是单文件实现，你只需将 `gamble.html` 中的内容复制到你的项目中，或者直接通过 iframe 引入：

```html
<iframe src="gamble.html" width="100%" height="500px" frameborder="0"></iframe>

```

### 自定义配置

在代码头部的 `:root` 标签中，你可以修改基础参数：

```css
:root {
    --ark-orange: #d64531;  /* 修改主题色 */
    --ticket-w: 70px;       /* 修改签位宽度 */
    --ticket-gap: 34px;     /* 修改签位间距 */
}

```

## 📂 目录结构

```text
.
├── gamble.html      # 核心逻辑文件 (HTML/CSS/JS 合一)
└── README.md        # 项目说明文档

```

## 📅 更新计划

* [ ] 增加多种主题颜色切换（暗黑模式/极光绿）
* [ ] 接入 Web Audio API，添加抽奖音效
* [ ] 支持后端 API 异步获取中奖结果

## 📄 开源协议

根据 [MIT License](https://www.google.com/search?q=LICENSE) 许可进行分发。
