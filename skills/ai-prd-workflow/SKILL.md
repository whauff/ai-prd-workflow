---
name: ai-prd-workflow
description: 当用户希望把一个需求收口为可评审、可共享的 PRD 交付包时使用。该 skill 负责判断阶段、选择产物、读取子 skill，并控制最终交付结构，不直接承载所有产出细节。
---

# ai-prd-workflow

把一个需求收口成一套可评审、可共享的交付包。这个 skill 是主编排层，负责判断当前阶段、补最小缺口、决定下一步该读取哪个子 skill，以及控制最终交付结构。

## 适用场景

- 需求需要多人协作和评审。
- 用户希望得到 PRD 及相关交付物。
- 需求适合通过 PRD、原型、规则稿或流程图来收敛分歧。
- 最终输出需要有清晰的统一入口。

## 不适用场景

- 只是很小的文案修改或轻微调整。
- 任务本质上是技术设计或实现规划。
- 还处于大范围发散探索，连问题边界都未形成。

## 工作守则

1. 先看已有上下文，再决定是否追问。
2. 主 skill 只负责判断阶段、选择子 skill、控制交付边界。
3. 默认交付保持克制：交付首页 + 完整 PRD。
4. 原型、规则稿、流程图都按需追加，不按习惯堆产物。
5. 如果没有新增分歧，就不要新增交付物。
6. 每轮都做减法检查，删除重复入口、重复说明和不可共享内容。
7. 不扩展到前后端职责、API 设计或技术实现方案。
8. 所有输出都按“可共享”组织：结构稳定、使用相对路径、入口清晰。

## 编排流程

### 1. 盘点上下文

先阅读 [shared/references/context-checklist.md](shared/references/context-checklist.md)，只识别那些会影响方案方向的缺口。

### 2. 判断当前阶段

按以下顺序判断：

- 如果背景、目标、用户、场景、现状、成功标准仍有关键缺口，进入“需求澄清阶段”。
- 如果需求已经足够清楚，进入“PRD 产出阶段”。
- 如果用户特别要求原型、规则稿或流程图，或内容确实触发这些产物，再进入对应追加阶段。

### 3. 读取对应子 skill

按阶段只读取必要的子 skill：

- 需求澄清：读取 [clarify-requirement/SKILL.md](clarify-requirement/SKILL.md)
- PRD 产出：读取 [write-prd/SKILL.md](write-prd/SKILL.md)
- 原型追加：读取 [build-prototype/SKILL.md](build-prototype/SKILL.md)
- 原型样式统一：读取 [style-prototype/SKILL.md](style-prototype/SKILL.md)
- 规则稿追加：读取 [write-rules/SKILL.md](write-rules/SKILL.md)
- 流程图追加：读取 [make-flowchart/SKILL.md](make-flowchart/SKILL.md)

不要在同一轮无必要地同时展开多个子 skill。优先顺序如下：

1. 先澄清
2. 再 PRD
3. 再按需追加原型、原型样式统一、规则稿或流程图

如果 PRD 已经足够清楚，就不要为了完整而强行补后续产物。

### 4. 判断交付范围

阅读 [shared/references/deliverable-triggers.md](shared/references/deliverable-triggers.md)，判断是否只交付 PRD，还是还需要追加：

- 原型
- 规则稿
- Mermaid 流程图

调度规则如下：

- 页面、表单、状态或布局是主要讨论对象时，再读取 `build-prototype`
- 原型结构已基本稳定，但交付样式需要统一时，再读取 `style-prototype`
- 识别、校验、拦截、打标、评分或分类判断会影响协作时，再读取 `write-rules`
- 逻辑分支、同步链路、异常分支已经不适合只用文字表达时，再读取 `make-flowchart`
- 如果只是轻微补充说明，不新增子 skill

### 5. 收口输出

最终交付前，阅读 [shared/references/reduction-checklist.md](shared/references/reduction-checklist.md)，删除重复入口、重复说明、本地路径耦合和不适合共享的内容。

## 默认交付判断

### 默认产物

- 交付首页
- 完整 PRD

### 追加原型的条件

- 需求涉及页面、表单、状态或布局。
- 交互本身是主要讨论对象。
- 团队大概率会在界面或行为上产生分歧。

### 追加原型样式统一的条件

- 需要统一原型的字体、层级、间距、状态表达。
- 多人协作导致原型视觉质量不稳定。
- 原型将被广泛分享或反复评审，需要统一交付标准。

### 追加规则稿的条件

- 需要定义什么算对、什么算错。
- 系统需要拦截、提示、打标、评分或分类。
- 边界样本或基于样本的判断会影响协作。

### 追加流程图的条件

- 逻辑存在关键分支。
- 有保存前或保存后的处理链路。
- 有同步、解析、回写或异常分支。
- 文字说明已经开始不如图示清楚。

### 停止扩产物的条件

- 核心问题、目标和方案已经清楚。
- 当前协作对象已经有足够材料。
- 没有新增分歧。
- 新文件只会重复现有内容。

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
