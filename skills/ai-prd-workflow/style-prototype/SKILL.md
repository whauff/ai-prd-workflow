---
name: style-prototype
description: 当原型结构和交互已经基本稳定，但团队需要统一视觉质量、排版、间距和状态表达时使用。负责把原型整理到统一交付标准，不改业务逻辑，不扩展为自由发挥的视觉设计。
---

# style-prototype

只做原型交付样式统一。目标是让不同同事产出的原型在评审时看起来属于同一套标准。

## 前提

只有在以下条件基本成立时才进入本 skill：

- 原型结构已经基本稳定
- 关键页面和关键状态已经存在
- 当前主要问题是样式质量不稳定，而不是业务逻辑不清楚

如果连页面结构都还在大改，应先回到 `build-prototype`。

## 读取文件

开始产出前按需读取：

- [../shared/references/prototype-style-standard.md](../shared/references/prototype-style-standard.md)
- [../shared/references/prototype-guidelines.md](../shared/references/prototype-guidelines.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)

## 工作方式

1. 只优化交付样式，不改变业务逻辑和页面结构目标。
2. 优先统一字体层级、间距节奏、颜色语义、表单与按钮样式。
3. 补齐空状态、错误态、禁用态、加载态等关键状态表达。
4. 让原型看起来专业、克制、稳定，而不是追求强烈视觉风格。
5. 如果某个视觉改动会改变业务理解，应明确提示需要同步回写 PRD 或原型说明。

## 输出

输出应至少包含：

- 本轮统一了哪些样式维度
- 哪些页面或模块已达到交付标准
- 哪些地方仍建议继续优化
- 是否需要同步更新 PRD 中的截图、说明或状态描述

## 边界

- 不改业务逻辑。
- 不新增功能。
- 不把原型升级为正式前端工程。
- 不追求作品集式或品牌大片式设计表达。
