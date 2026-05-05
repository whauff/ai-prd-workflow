---
name: make-flowchart
description: 当文字已经不足以表达关键分支、处理链路或异常路径，需要用 Mermaid 流程图来帮助评审时使用。只负责把关键逻辑画清楚，不扩展成系统架构图。
---

# make-flowchart

只做帮助评审的 Mermaid 流程图，重点是把关键路径和关键分支画清楚。

## 前提

只有在以下情况成立时才进入本 skill：

- 逻辑存在关键分支
- 保存前后有处理链路
- 存在同步、解析、回写或异常处理
- 仅靠文字描述已经不够清楚

如果逻辑简单到一段话就能说清，就不要强行画图。

## 读取文件

开始产出前按需读取：

- [../shared/references/flowchart-guidelines.md](../shared/references/flowchart-guidelines.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)

## 工作方式

1. 先确定图是服务哪一段逻辑，不要一张图包打天下。
2. 只画会影响协作判断的节点和分支。
3. 正常路径和异常路径都要清楚，但不要把图画成全量技术蓝图。
4. 节点文案保持短、稳、可读。
5. 如果一张图已经过大，应拆成多张小图，而不是继续加节点。

## 输出

输出应至少包含：

- 这张图覆盖的范围
- Mermaid 图代码
- 对关键分支或异常分支的简短说明

## 边界

- 不画系统架构图。
- 不把研发实现细节塞进节点。
- 不为了形式完整而画重复图。
