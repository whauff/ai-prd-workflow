---
name: write-prd
description: 当需求已经足够清楚，需要整理为完整、可评审的 PRD 时使用。负责基于共享模板生成或更新 PRD，不扩展到原型、流程图或技术实现。
---

# write-prd

把已澄清、已定口径的需求整理成 PRD。

## 前提

进入条件：

- 背景已经清楚
- 目标已经清楚
- 用户和场景基本清楚
- 现状和成功标准至少有初步共识
- 本期范围、判断顺序、字段层级、多端权限和关键规则边界已定，或已有 Brief 结论可沿用

如果仍存在关键缺口，应先回到需求澄清阶段。
如果范围、顺序、字段、权限或规则边界还未定，不直接起 PRD，先回到 [../review-brief/SKILL.md](../review-brief/SKILL.md)。

若已有 Brief，以 Brief 为口径基准，不改范围、顺序、字段、权限或拍板结论。

## 读取文件

开始产出前按需读取：

- [../shared/templates/prd-template.md](../shared/templates/prd-template.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)
- [../shared/references/deliverable-triggers.md](../shared/references/deliverable-triggers.md)

规则、治理、识别、校验、分类、计算、分配、结算、权益、价格或优先级需求，可补充读取：

- [../shared/references/sample-analysis-guide.md](../shared/references/sample-analysis-guide.md)

## 工作方式

1. 按模板组织，不从空白发散。
2. 优先把背景、目标、用户场景、核心方案和边界写清楚。
3. 对尚未确认的内容，明确标记“待确认”，不要伪造确定性。
4. 语言克制、业务化、可评审。
5. 不扩展到前后端职责、API、表结构或研发实现细节。
6. 若存在独立规则稿，PRD 只保留规则摘要和链接，不重复承载复杂规则明细。
7. 规则摘要只回答三件事：为什么需要这套规则、影响哪些对象或场景、详细口径见哪份规则稿。
8. 若存在独立规则稿，PRD 正文不得再展开规则矩阵、命中条件、计算明细、优先级或例外。
9. 完成后运行减法检查。

## 输出

输出应至少包含：

- 一份完整 PRD 初稿或更新稿
- 明确标记的待确认项
- 对是否需要原型、规则稿、流程图作为独立交付物的判断

## 独立交付物判断

完成后说明：

- 是否需要原型
- 是否需要规则稿
- 是否需要流程图

建议独立交付时说明触发原因。

## 边界

- 不直接生成原型。
- 不直接生成 Mermaid 流程图。
- 不拆研发任务。
- 不写技术实现方案。
