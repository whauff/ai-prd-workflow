# ai-prd-workflow cheatsheet

## 入口

| 情况 | 调用 |
|---|---|
| 不确定从哪开始 | `ai-prd-workflow` |
| 缺背景、目标、用户、场景或成功标准 | `clarify-requirement` |
| 需先定范围、顺序、字段或权限 | `review-brief` |
| 需完整 PRD | `write-prd` |
| 页面或交互影响评审 | `build-prototype` |
| 原型结构稳定但样式不统一 | `style-prototype` |
| 复杂业务规则需独立评审、复用或维护 | `write-rules` |
| 分支、链路或异常路径文字说不清 | `make-flowchart` |

## 卡点

- 用户直接说“写 PRD”，但范围、顺序、字段、权限或规则边界没定：先走 `review-brief`。
- 地址治理、状态检查、识别校验类需求：不因有规则就默认拆规则稿，只有规则复杂且需独立评审、复用或持续维护时才进入 `write-rules`。
- 已有独立规则稿：PRD 只保留规则摘要和链接，不再展开规则矩阵、计算明细、优先级和例外。

## 顺序

```text
ai-prd-workflow → clarify-requirement → review-brief → 确定正式交付物组合 → 按需进入 PRD / 原型 / 规则稿 / 流程图
```

这是判断顺序，不是固定流水线。

## 停止

- PRD 已清楚，原型无新增评审价值。
- 规则不复杂，不拆规则稿。
- 逻辑一句话能说清，不画流程图。
- 问题属于技术实现，不走 PRD 交付。

## 句式

```text
请使用 ai-prd-workflow，先判断这个需求该怎么收口：
……
```

```text
请使用 review-brief，先确认范围、判断顺序、字段层级和待拍板问题：
……
```

```text
请使用 write-rules，把这部分复杂业务规则口径整理成独立规则稿：
……
```
