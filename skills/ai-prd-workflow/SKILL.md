---
name: ai-prd-workflow
description: 当用户希望把一个需求收口为可评审、可共享的 PRD 交付包时使用。该 skill 负责最高编排：确立原则、识别需求类型、决定阶段顺序、调度子 skill、控制边界和最终收口。
---

# ai-prd-workflow

最高编排层。负责原则、分类、阶段、调度和收口，不替代子 skill 生成具体产物。

## 基础原则

| 原则 | 定义 | 执行要求 |
|---|---|---|
| 高效 | 先抓关键口径，减少无效澄清和无效产物 | 默认先 Brief，后 PRD |
| 简洁 | 只保留有决策价值的信息 | 短版表达；不命中不占位；删除空话、重复解释 |
| 严谨 | 不混层、不脑补、不越过未确认边界 | 先确认范围、判断顺序、字段层级、多端权限；未确认能力不得写入 |
| 可持续 | 标准持续一致 + 产物可维护 | 全流程命名、口径、顺序、字段、边界一致；旧产物有归档或删除策略 |
| 可复制 | 需求自动分类，按统一流程产出，用统一标准检查质量 | 自动识别类型；同类需求走统一流程；交付质量可逐项检查 |

## 需求分类

用户不需要预先分类。先判断是否命中：

- 规则型：判断、计算、分配、结算、权益、价格、优先级、例外。
- 流程型：提交、审核、派单、回访、复核、流转、撤回、驳回。
- 页面交互型：页面、表单、列表、筛选、详情、弹窗、按钮、提示。
- 状态表达型：总状态、检查项状态、原因类型、处理建议、标签、提示文案。
- 多端权限型：多端、多角色、可见范围、可处理范围、关键动作权限。

一个需求可以命中多类。

## 阶段顺序

默认顺序：

1. 澄清
2. 评审 Brief
3. 正式交付
4. 同步检查与收口

阶段规则：

- 关键事实不足：先澄清。
- 需要确认范围、判断顺序、字段层级、多端权限或争议边界：先 Brief。
- Brief 有待拍板问题：停，等用户确认。
- Brief 无待拍板问题：可继续交付，并说明“基于当前 Brief 默认展开”。
- 下游出现新判断：回到 Brief 更新口径。

## 子 skill 调度

按需读取，不全量展开：

| 阶段 / 触发 | 子 skill |
|---|---|
| 需求缺关键上下文 | [clarify-requirement/SKILL.md](clarify-requirement/SKILL.md) |
| 需要先定口径 | [review-brief/SKILL.md](review-brief/SKILL.md) |
| 需要完整 PRD | [write-prd/SKILL.md](write-prd/SKILL.md) |
| 页面、表单、状态或交互影响评审 | [build-prototype/SKILL.md](build-prototype/SKILL.md) |
| 原型结构稳定但样式需统一 | [style-prototype/SKILL.md](style-prototype/SKILL.md) |
| 复杂业务规则需独立评审、复用或维护 | [write-rules/SKILL.md](write-rules/SKILL.md) |
| 关键分支、处理链路或异常路径文字说不清 | [make-flowchart/SKILL.md](make-flowchart/SKILL.md) |

规则稿不是默认产物。只有复杂业务规则口径需要独立评审、复用或持续维护时才追加。

## 全局底线

- 未确认的系统能力不得写入交付物，例如自动检测、智能识别、自动修复。
- 不写前后端职责、API、表结构或研发实现方案。
- 多交付物必须检查命名、状态、判断顺序、范围前提、字段层级和链接一致性。
- 收尾时明确最终交付、待归档内容和应删除内容；默认只暴露最终版入口。

## 共享文件

### 模板

- [shared/templates/prd-template.md](shared/templates/prd-template.md)
- [shared/templates/rules-template.md](shared/templates/rules-template.md)
- [shared/templates/delivery-index-template.md](shared/templates/delivery-index-template.md)

### 参考文件

- [shared/references/context-checklist.md](shared/references/context-checklist.md)
- [shared/references/deliverable-triggers.md](shared/references/deliverable-triggers.md)
- [shared/references/prototype-guidelines.md](shared/references/prototype-guidelines.md)
- [shared/references/prototype-style-standard.md](shared/references/prototype-style-standard.md)
- [shared/references/reduction-checklist.md](shared/references/reduction-checklist.md)
- [shared/references/sample-analysis-guide.md](shared/references/sample-analysis-guide.md)
- [shared/references/flowchart-guidelines.md](shared/references/flowchart-guidelines.md)
