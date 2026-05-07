# ai-prd-workflow

组合式产品需求收口工作流 skill。把零散需求收口为可评审、可共享的正式交付；按需组织 Brief、PRD、原型、规则稿和流程图。

## 仓库结构

```text
.
├── README.md
├── docs/
│   ├── CHEATSHEET.md
│   ├── EXAMPLES.md
│   ├── STYLE_GUIDE.md
│   └── USAGE.md
└── skills/
    └── ai-prd-workflow/
        ├── SKILL.md
        ├── agents/openai.yaml
        ├── clarify-requirement/
        ├── review-brief/
        ├── write-prd/
        ├── build-prototype/
        ├── style-prototype/
        ├── write-rules/
        ├── make-flowchart/
        └── shared/
```

## 安装

使用 Codex 自带的 `skill-installer` 安装：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo whauff/ai-prd-workflow \
  --path skills/ai-prd-workflow
```

安装后重启 Codex。

## 适用场景

- 需求零散，需要澄清
- 正式交付前需先收口关键口径
- 需要按需组织 PRD、原型、规则稿或流程图
- 复杂业务规则需独立沉淀

## 文档

- [使用说明](docs/USAGE.md)
- [调用速查表](docs/CHEATSHEET.md)
- [调用示例](docs/EXAMPLES.md)
- [原型样式说明](docs/STYLE_GUIDE.md)
