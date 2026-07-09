# 前置入口路由

用于区分 `grill-me`、`clarify-requirement`、`review-brief` 三个 PRD 前入口。先判断用户此刻真正需要的是：挑战方向、补齐事实，还是拍板口径。

## 一句话判定

| 入口 | 核心问题 | 用户状态 | 产出 |
|---|---|---|---|
| `grill-me` | 这件事值不值得继续？ | 有想法或方案，倾向推进，但关键假设未被挑战 | 尖锐结论、脆弱点、追问、下一步验证 |
| `clarify-requirement` | 这件事到底是什么？ | 背景、目标、用户、场景、现状或成功标准缺失 | 已知信息、待确认问题、结构化摘要、阶段判断 |
| `review-brief` | 这件事按什么口径做？ | 关键事实基本具备，但范围、顺序、字段、权限或边界未拍板 | 短版拍板单、范围边界、判断顺序、待拍板问题 |

## 优先级

1. 用户明确要求拷问、挑战、找漏洞、压力测试：进 `grill-me`。
2. 用户没有要求拷问，且关键事实缺失：进 `clarify-requirement`。
3. 关键事实基本具备，但下游交付口径未定：进 `review-brief`。
4. 方向、事实和口径都稳定：再进入 PRD、规则稿、原型或流程图。

## 不互相抢活

### grill-me 不做

- 不补全完整背景摘要；信息缺失只列最关键追问。
- 不整理拍板单；边界问题只指出风险。
- 不把想法包装成 PRD。

### clarify-requirement 不做

- 不判断值不值得做，除非缺口本身说明方向不成立。
- 不输出范围、字段、权限等拍板口径。
- 不直接展开 PRD。

### review-brief 不做

- 不重新拷问方向是否值得做；若方向明显未验证，退回 `grill-me`。
- 不补基础背景；关键事实不足时退回 `clarify-requirement`。
- 不写完整交付物。

## 典型例子

| 用户输入 | 应进入 | 不进入 | 原因 |
|---|---|---|---|
| 我有个想法，帮我看看值不值得做 | `grill-me` | `clarify-requirement` / `review-brief` | 用户要挑战方向，不是补材料或定口径 |
| 这个方案看起来对，但我怕有坑 | `grill-me` | `review-brief` | 先找隐藏假设和失败信号 |
| 帮我把这个零散需求理清楚 | `clarify-requirement` | `grill-me` | 用户需要结构化事实，不是高压质询 |
| 现在只有一句话需求：医生端想看患者标签 | `clarify-requirement` | `review-brief` | 背景、用户、场景、成功标准不足 |
| 目标和场景都清楚了，帮我定本期做哪些、不做哪些 | `review-brief` | `clarify-requirement` | 事实具备，缺的是范围口径 |
| 这个状态要怎么分总状态、检查项状态、原因类型 | `review-brief` | `clarify-requirement` | 要定字段层级和判断顺序 |
| 直接写 PRD，但范围、权限、判断顺序还没定 | `review-brief` | `write-prd` | 先拍板口径，避免长 PRD 伪进展 |
| 直接写 PRD，我还没想清谁用、为什么做 | `clarify-requirement` | `write-prd` / `review-brief` | 先补关键事实 |
| 我们要不要做这个功能，先别写文档 | `grill-me` | `clarify-requirement` | 用户要决策压力测试 |

## 退回规则

- `grill-me` 后发现方向可继续但事实缺：转 `clarify-requirement`。
- `grill-me` 后方向成立且事实具备但口径未定：转 `review-brief`。
- `clarify-requirement` 中发现用户其实要找漏洞：停，转 `grill-me`。
- `review-brief` 中发现基础事实不足：停，转 `clarify-requirement`。
- `review-brief` 中发现方向价值未验证：停，转 `grill-me`。
