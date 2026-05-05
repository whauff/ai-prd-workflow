# ai-prd-workflow

一套面向需求收口与 PRD 交付的组合式 skill。采用“主 skill 编排 + 子 skill 执行 + shared 共享模板”的结构，便于团队复用和后续扩展。

## 这套 skill 解决什么问题

它适合把一个零散、口语化、尚未完全收口的需求，逐步整理成可评审、可共享的交付物。核心目标不是“生成很多文件”，而是让团队更快对齐：

- 当前到底要解决什么问题
- 为什么现在做
- 谁在什么场景下使用
- 方案是否已经足够清楚进入评审
- 是否还需要原型、规则稿或流程图

## 适合什么场景

- 需求刚形成，信息还零散，需要先澄清
- 需要把对话、会议纪要、截图整理成 PRD
- 页面或交互会引起较大分歧，需要补原型
- 存在识别、校验、拦截、打标、评分等规则口径
- 逻辑链路或异常分支较多，文字已经不够清楚

## 不适合什么场景

- 只是改一句文案、调一个标题、补一个按钮说明
- 本质上是在做技术设计、接口设计或研发实现方案
- 还处于纯发散阶段，连问题边界都没有形成
- 只是要一个最终视觉稿，而不是业务评审交付物

## 目录结构

- `SKILL.md`
  - 主 skill。负责判断阶段、决定交付范围、读取子 skill。
- `clarify-requirement/`
  - 子 skill。负责补关键上下文缺口并输出结构化需求摘要。
- `write-prd/`
  - 子 skill。负责基于共享模板生成或更新 PRD。
- `build-prototype/`
  - 子 skill。负责产品交付视角的原型。
- `style-prototype/`
  - 子 skill。负责统一原型交付样式。
- `write-rules/`
  - 子 skill。负责生成独立规则稿。
- `make-flowchart/`
  - 子 skill。负责生成 Mermaid 流程图。
- `shared/templates/`
  - 共享模板。
- `shared/references/`
  - 共享判断规则与检查清单。

## 推荐用法

### 直接使用主 skill

适合大多数场景。由主 skill 判断当前该先澄清需求，还是直接产出 PRD，并决定是否追加原型、原型样式统一、规则稿或流程图。

### 单独使用子 skill

适合已经明确知道自己要做哪一步：

- 需求还模糊：使用 `clarify-requirement`
- 需求已经清楚：使用 `write-prd`
- 页面或交互是重点：使用 `build-prototype`
- 原型结构已定，但视觉质量需要统一：使用 `style-prototype`
- 规则口径需要单独对齐：使用 `write-rules`
- 逻辑分支需要图示：使用 `make-flowchart`

## 最小使用方式

如果不确定该怎么用，默认按下面这个最小路径：

1. 先使用 `ai-prd-workflow`
2. 如果主 skill 判断信息不够，就进入 `clarify-requirement`
3. 信息够了以后，进入 `write-prd`
4. 只有在确实触发时，才追加 `build-prototype`、`style-prototype`、`write-rules`、`make-flowchart`

这套 skill 的默认原则是：先收口，再扩产物。

## 设计原则

- 主 skill 只做编排，不把所有细节塞进一个文件。
- 子 skill 各自只做一件事，避免职责重叠。
- 模板和参考文件只保留一份，降低维护成本。
- 所有引用优先走相对路径，避免个人环境耦合。

## 推荐顺序

大多数需求推荐按这个顺序使用：

1. `ai-prd-workflow`
2. `clarify-requirement`
3. `write-prd`
4. 视情况追加 `build-prototype`
5. 如原型已形成，视情况追加 `style-prototype`
6. 视情况追加 `write-rules`
7. 视情况追加 `make-flowchart`

## 什么时候不要全跑一遍

不要把这套 skill 当成固定流水线。以下情况应停止扩展：

- PRD 已经足够清楚，继续补原型只会重复
- 原型还没成型前，不要过早进入 `style-prototype`
- 需求没有复杂规则，没必要单独写规则稿
- 逻辑很简单，一段文字比画流程图更快
- 当前协作对象只需要一个 PRD，不需要更多包装

## 常见调用示例

### 示例 1：需求还很模糊

输入：一段聊天记录，外加一句“想优化小程序状态检查”

推荐：

1. `ai-prd-workflow`
2. `clarify-requirement`
3. `write-prd`

### 示例 2：PRD 已经有了，但交互容易吵起来

输入：一份已有 PRD，大家对页面状态和按钮反馈有分歧

推荐：

1. `build-prototype`
2. `style-prototype`
3. 如原型影响方案，再同步更新 `write-prd`

### 示例 3：核心争议在规则口径

输入：一份需求说明，争议点在“什么情况要拦截，什么情况只提示”

推荐：

1. `write-prd`
2. `write-rules`
3. 如分支很多，再补 `make-flowchart`

## 给同事的使用提醒

- 不确定从哪开始时，先用 `ai-prd-workflow`
- 不要为了完整而强行把所有子 skill 都跑一遍
- 如果当前已经是明确需求，直接从 `write-prd` 开始更高效
- 如果只是局部补充，不要重跑整套流程
- `style-prototype` 只解决统一交付样式，不解决业务逻辑问题

## 后续可继续追加

- `delivery-index`
