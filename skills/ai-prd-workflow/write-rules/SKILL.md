---
name: write-rules
description: 当需求涉及识别、校验、拦截、提示、打标、评分或分类判断，需要单独对齐规则口径时使用。负责生成独立规则稿，不扩展为规则引擎技术设计。
---

# write-rules

把规则从 PRD 中拆出来，单独对齐判断口径、处理策略和边界样本。

## 前提

只有在以下情况成立时才进入本 skill：

- 规则本身会影响评审或协作结论
- 不同人对什么算命中、什么算误伤可能有分歧
- 边界样本会直接影响处理方式

如果规则只是轻微补充说明，优先留在 PRD 中简要表达。

## 读取文件

开始产出前按需读取：

- [../shared/templates/rules-template.md](../shared/templates/rules-template.md)
- [../shared/references/sample-analysis-guide.md](../shared/references/sample-analysis-guide.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)

## 工作方式

1. 优先基于真实样本、真实风险和真实争议点写规则。
2. 每条规则都要能回答“为什么这样判”和“命中后怎么处理”。
3. 规则稿应聚焦判断口径，不扩展成小 PRD。
4. 如果尚无足够样本，应明确指出缺失样本会影响哪部分判断。
5. 对高争议边界，优先写清误伤风险和兜底策略。

## 输出

输出应至少包含：

- 规则目标
- 规则决策表
- 判断信号
- 边界样本
- 处理策略
- 当前版本覆盖范围和待补部分

## 边界

- 不写规则引擎实现。
- 不写接口或数据表设计。
- 不把所有业务方案都重复抄进规则稿。
