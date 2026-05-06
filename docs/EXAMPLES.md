# ai-prd-workflow examples

## 模糊需求

输入：

```text
想做小程序状态检查，避免门店提交错误配置，但还没想清哪些状态拦截、哪些只提醒。
```

入口：

```text
ai-prd-workflow → clarify-requirement → review-brief → write-prd → write-rules
```

原因：目标和边界未定，且存在规则口径。

## 明确需求

输入：

```text
需求已讨论完，整理成可评审 PRD，重点写背景、目标、用户场景和验收标准。
```

入口：

```text
write-prd
```

原因：无需澄清，产物明确。

## 交互争议

输入：

```text
PRD 已有，页面状态提示、按钮文案和异常反馈有分歧，想先看可评审原型。
```

入口：

```text
build-prototype → style-prototype → 必要时回写 write-prd
```

原因：争议集中在界面行为。

## 复杂规则

输入：

```text
定义互联网医院不同市场投放下的分佣规则，不同主体、渠道来源和订单类型对应不同结算口径。
```

入口：

```text
review-brief → write-prd → write-rules
```

原因：多主体、多场景、多条件组合，需要独立评审和持续维护。

## 复杂链路

输入：

```text
保存前校验，保存后同步、回写并处理异常，评审时总有人理解不一样。
```

入口：

```text
make-flowchart → 必要时回写 write-prd
```

原因：分支和异常路径需要图示。
