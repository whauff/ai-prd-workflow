---
name: make-flowchart
description: 当文字已经不足以表达关键分支、处理链路或异常路径，需要用 Mermaid 流程图来帮助评审时使用。只负责把关键逻辑画清楚，不扩展成系统架构图。
---

# make-flowchart

只做帮助评审的 Mermaid 流程图，画清关键路径和分支。

## 前提

只有在以下情况成立时才进入本 skill：

- 逻辑存在关键分支
- 保存前后有处理链路
- 存在同步、解析、回写或异常处理
- 仅靠文字描述已经不够清楚

一段话能说清时，不画图。

若已有 Brief，以 Brief 为口径基准，不改范围、顺序、字段、权限或拍板结论。

## 读取文件

开始产出前按需读取：

- [../shared/references/flowchart-guidelines.md](../shared/references/flowchart-guidelines.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)

## 工作方式

1. 先确定图覆盖哪段逻辑。
2. 只画影响协作判断的节点和分支。
3. 正常路径和异常路径都要清楚，但不要把图画成全量技术蓝图。
4. 原型审查中暴露出的异常路径、状态跳转或处理分支，可作为流程图触发来源。
5. 节点文案保持短、稳、可读。
6. 图过大时拆图。

## 输出

输出应至少包含：

- 这张图覆盖的范围
- Mermaid 图代码
- 对关键分支或异常分支的简短说明

## 边界

- 不画系统架构图。
- 不把研发实现细节塞进节点。
- 不为了形式完整而画重复图。
