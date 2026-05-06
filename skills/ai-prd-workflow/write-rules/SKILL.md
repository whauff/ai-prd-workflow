---
name: write-rules
description: 当需求包含复杂业务规则口径，且该规则需要独立评审、复用或持续维护时使用。负责生成独立规则稿，不扩展为规则引擎技术设计。
---

# write-rules

把复杂业务规则从 PRD 中拆出，单独对齐判断、计算、分配、适配、优先级、例外和处理策略。

## 前提

只有在以下情况成立时才进入本 skill：

- 规则影响评审或协作结论
- 规则存在多条件组合、多主体差异、多场景适配、优先级或例外情况
- 规则会被多个页面、端、流程复用
- 规则需持续维护
- 放在 PRD 中会让正文复杂、难评审

如果规则只是轻微补充说明，优先留在 PRD 中简要表达。

若已有 Brief，以 Brief 为口径基准，不改范围、顺序、字段、权限或拍板结论。

## 读取文件

开始产出前按需读取：

- [../shared/templates/rules-template.md](../shared/templates/rules-template.md)
- [../shared/references/sample-analysis-guide.md](../shared/references/sample-analysis-guide.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)

## 工作方式

1. 基于真实样本、风险、争议点和已确认口径写规则。
2. 判断类规则要回答“为什么这样判”和“命中后怎么处理”。
3. 计算、分配、适配类规则要回答“不同条件组合下结果如何确定”。
4. 样本不足时，指出影响哪部分判断。
5. 规则稿应聚焦规则口径，不扩展成小 PRD。
6. 高争议边界、优先级冲突和例外情况，优先写清处理策略。

## 输出

输出应至少包含：

- 规则目标
- 规则决策表或规则矩阵
- 判断信号或适用条件
- 边界样本或规则示例
- 处理策略
- 优先级和例外情况
- 当前版本覆盖范围和待补部分

## 边界

- 不写规则引擎实现。
- 不写接口或数据表设计。
- 不把所有业务方案都重复抄进规则稿。
