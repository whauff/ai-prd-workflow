# ai-prd-workflow

组合式需求收口 skill：主 skill 编排，子 skill 执行，shared 复用模板和检查清单。

## 目标

把零散需求收口成可评审、可共享的交付物。重点对齐：

- 问题、目标、用户、场景
- 范围、判断顺序、字段层级、权限口径
- 是否需要 PRD、原型、规则稿或流程图

## 入口

| 情况 | 使用 |
|---|---|
| 不确定从哪开始 | `ai-prd-workflow` |
| 缺背景、目标、用户、场景或成功标准 | `clarify-requirement` |
| 需要先定范围、顺序、字段或权限 | `review-brief` |
| 需要完整 PRD | `write-prd` |
| 页面或交互影响评审 | `build-prototype` |
| 原型结构稳定但样式不统一 | `style-prototype` |
| 复杂业务规则需独立评审、复用或维护 | `write-rules` |
| 分支、链路或异常路径文字说不清 | `make-flowchart` |

## 推荐顺序

1. `ai-prd-workflow`
2. `clarify-requirement`
3. `review-brief`
4. `write-prd`
5. 按需追加 `build-prototype`、`style-prototype`、`write-rules`、`make-flowchart`

这是判断顺序，不是固定流水线。

## 原则

- 高效：先抓关键口径，减少无效澄清和无效产物。
- 简洁：只保留有决策价值的信息。
- 严谨：不混层、不脑补、不越过未确认边界。
- 可持续：标准持续一致 + 产物可维护。
- 可复制：需求自动分类，按统一流程产出，用统一标准检查质量。

## 停止条件

- PRD 已经足够清楚，原型没有新增评审价值。
- 规则不复杂，不需要独立规则稿。
- 逻辑一段话能说清，不需要流程图。
- 当前问题是技术实现，不是产品交付。

## 示例

### 模糊需求

```text
ai-prd-workflow → clarify-requirement → review-brief → write-prd
```

### 交互争议

```text
build-prototype → style-prototype → 必要时回写 write-prd
```

### 复杂规则

```text
review-brief → write-prd → write-rules → 必要时 make-flowchart
```
