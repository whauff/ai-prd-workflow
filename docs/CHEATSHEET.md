# ai-prd-workflow cheatsheet

一页式调用决策表。目标是快速判断：现在该调用哪个 skill。

## 默认原则

- 不确定从哪开始：先用 `ai-prd-workflow`
- 已经知道卡在哪一段：直接用对应子 skill
- 不要为了完整把所有 skill 都跑一遍

## 决策表

| 当前情况 | 直接调用 | 说明 |
| --- | --- | --- |
| 需求还很散，不知道先做什么 | `ai-prd-workflow` | 让主 skill 先判断阶段和交付范围 |
| 需求模糊，缺背景/目标/用户/场景/成功标准 | `clarify-requirement` | 先补关键缺口，不直接写 PRD |
| 需求已经清楚，需要整理成可评审文档 | `write-prd` | 直接产出或更新 PRD |
| 页面、表单、状态、交互是争议重点 | `build-prototype` | 用原型收敛界面和行为分歧 |
| 原型已经有了，但字体、间距、状态、组件风格不统一 | `style-prototype` | 只统一交付样式，不改业务逻辑 |
| 核心争议在识别/校验/拦截/打标/评分规则 | `write-rules` | 单独整理规则口径和边界样本 |
| 逻辑分支、同步链路、异常处理说不清 | `make-flowchart` | 用 Mermaid 画清主流程和异常分支 |

## 推荐顺序

大多数需求按这个顺序判断：

1. `ai-prd-workflow`
2. `clarify-requirement`
3. `write-prd`
4. `build-prototype`
5. `style-prototype`
6. `write-rules`
7. `make-flowchart`

注意：这是判断顺序，不是每次都要全跑。

## 常见组合

### 组合 1：从模糊想法到 PRD

1. `ai-prd-workflow`
2. `clarify-requirement`
3. `write-prd`

### 组合 2：PRD 已有，但交互要落图

1. `build-prototype`
2. `style-prototype`
3. 必要时回写 `write-prd`

### 组合 3：规则是重点

1. `write-prd`
2. `write-rules`
3. 必要时 `make-flowchart`

### 组合 4：只补样式标准

1. `style-prototype`

适用前提：

- 原型结构已稳定
- 当前问题是交付质量不一致

## 什么时候停止

出现以下情况就不要继续往下跑：

- PRD 已经足够清楚
- 原型没有新增评审价值
- 规则并不复杂
- 一段文字比流程图更清楚
- 当前问题其实是技术实现，不是产品交付

## 可直接复制的调用句式

### 不确定入口

```text
请使用 ai-prd-workflow，先判断这个需求该怎么收口：
……
```

### 先澄清

```text
请使用 clarify-requirement，帮我补齐关键缺口，不要直接写 PRD：
……
```

### 先写 PRD

```text
请使用 write-prd，把下面需求整理成一版可评审 PRD：
……
```

### 先出原型

```text
请使用 build-prototype，基于这版 PRD 出可评审原型，重点覆盖关键页面和状态：
……
```

### 统一原型样式

```text
请使用 style-prototype，按团队统一交付标准整理这个原型，不改业务逻辑，只统一样式、层级、间距和状态表达：
……
```

### 单独写规则稿

```text
请使用 write-rules，把这部分判断口径整理成独立规则稿：
……
```

### 单独画流程图

```text
请使用 make-flowchart，把这段逻辑整理成 Mermaid 流程图，重点画清主流程和异常分支：
……
```
