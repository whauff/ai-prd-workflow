---
name: build-prototype
description: 当页面、表单、状态或交互行为本身是主要讨论对象，需要用可预览的原型来收敛分歧时使用。只负责产品交付视角的原型，不扩展为通用前端工程实现。
---

# build-prototype

只做产品交付原型，帮助评审页面结构、关键状态和交互路径。

## 前提

只有在以下条件至少满足大部分时才进入本技能：

- 需求目标已经基本清楚
- 核心用户和场景已经清楚
- 主要页面或关键操作路径已经有初步定义

页面目标不清时，先回到澄清或 PRD。

若已有 Brief，以 Brief 为口径基准，不改范围、顺序、字段、权限或拍板结论。

## 读取文件

开始产出前按需读取：

- [../shared/references/prototype-guidelines.md](../shared/references/prototype-guidelines.md)
- [../shared/references/prototype-design-quality.md](../shared/references/prototype-design-quality.md)
- [../shared/references/reduction-checklist.md](../shared/references/reduction-checklist.md)

若已有 PRD，基于 PRD 产出。

## 工作方式

1. 只覆盖影响评审的页面和状态。
2. 优先表达主流程、异常状态、空状态、权限差异、关键反馈和状态流转。
3. 用原型审查发现文字方案里的遗漏，例如返回、撤回、失败、无权限、空数据和处理后状态。
4. 服务业务评审，不追求炫技或通用组件体系。
5. PRD 已讲清的内容，不在原型里重复堆说明。
6. 假数据保持真实业务感，不伪装成最终文案。
7. 演示控件与真实页面结构分层，不混入正式页面功能。
8. 原型代码应自带基础可用性：响应式布局、可读文字、完整交互状态和清楚的错误/空/加载态。

## 输出

输出应至少包含：

- 原型覆盖了哪些页面或场景
- 原型未覆盖哪些内容
- 关键状态说明
- 与 PRD、Brief 或流程图是否存在需要同步更新的差异

## 边界

- 不写技术实现方案。
- 不扩展到设计系统建设。
- 不为了美观而牺牲评审效率。
- 不把原型当成正式开发代码承诺。
- 不使用强风格化、炫技动画或作品集式视觉表达。
