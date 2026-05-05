---
name: write-prd
description: 当需求已经足够清楚，需要整理为完整、可评审的 PRD 时使用。负责基于共享模板生成或更新 PRD，不扩展到原型、流程图或技术实现。
---

# write-prd

把已澄清的需求整理成完整、可评审、可共享的 PRD。

## 前提

只有在以下条件基本成立时才进入本 skill：

- 背景已经清楚
- 目标已经清楚
- 用户和场景已经基本清楚
- 现状和成功标准至少有初步共识

如果仍存在关键缺口，应先回到需求澄清阶段。

## 读取文件

开始产出前按需读取：

- [../shared/templates/prd-template.md](../shared/templates/prd-template.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)
- [../shared/references/deliverable-triggers.md](../shared/references/deliverable-triggers.md)

如果需求偏规则、治理、识别、校验或分类判断，可补充读取：

- [../shared/references/sample-analysis-guide.md](../shared/references/sample-analysis-guide.md)

## 工作方式

1. 先按模板组织结构，不从空白开始随意发散。
2. 优先把背景、目标、用户场景、核心方案和边界写清楚。
3. 对尚未确认的内容，明确标记“待确认”，不要伪造确定性。
4. 语言保持克制、业务化、可评审，避免空泛的套话。
5. 不扩展到前后端职责、API、表结构或研发实现细节。
6. 完成后运行减法检查，删除重复表达和不可共享内容。

## 输出

输出应至少包含：

- 一份完整 PRD 初稿或更新稿
- 明确标记的待确认项
- 对是否需要追加原型、规则稿、流程图的判断

## 追加产物判断

完成 PRD 后，应额外说明以下判断：

- 是否建议追加原型
- 是否建议追加规则稿
- 是否建议追加流程图

如果建议追加，要说明触发原因，而不是只给结论。

## 边界

- 不直接生成原型。
- 不直接生成 Mermaid 流程图。
- 不拆研发任务。
- 不写技术实现方案。
