# ai-prd-workflow

组合式产品需求收口工作流技能。把零散需求收口为可评审、可共享的正式交付；按需组织 Brief、PRD、原型、规则稿和流程图。

## 仓库结构

```text
.
├── README.md
├── docs/
│   ├── CHEATSHEET.md
│   ├── EXAMPLES.md
│   ├── GOVERNANCE_BACKLOG.md
│   ├── STYLE_GUIDE.md
│   ├── TEAM_USAGE.md
│   └── USAGE.md
└── skills/
    └── ai-prd-workflow/
        ├── SKILL.md
        ├── agents/openai.yaml
        ├── grill-me/
        ├── clarify-requirement/
        ├── review-brief/
        ├── write-prd/
        ├── build-prototype/
        ├── review-prototype/
        ├── write-rules/
        ├── make-flowchart/
        └── shared/
```

## 安装

使用 Codex 自带的技能安装器安装：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo whauff/ai-prd-workflow \
  --path skills/ai-prd-workflow
```

安装后重启 Codex。

## 适用场景

- 需求零散，需要澄清
- 想法或方案需要先被拷问、挑战或压力测试
- 正式交付前需先收口关键口径
- 需要按需组织 PRD、原型、规则稿或流程图
- 复杂业务规则需独立沉淀

## 前置入口

- `grill-me`：挑战方向，判断值不值得继续。
- `clarify-requirement`：补齐事实，明确背景、目标、用户、场景和成功标准。
- `review-brief`：拍板口径，确认范围、顺序、字段、权限和边界。

## 文档

- [使用说明](docs/USAGE.md)
- [调用速查表](docs/CHEATSHEET.md)
- [调用示例](docs/EXAMPLES.md)
- [原型交付质量说明](docs/STYLE_GUIDE.md)
- [团队使用说明](docs/TEAM_USAGE.md)
- [治理待办](docs/GOVERNANCE_BACKLOG.md)
