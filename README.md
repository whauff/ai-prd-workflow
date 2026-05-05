# ai-prd-workflow

面向 Codex 的组合式产品需求工作流 skill。目标是把零散需求逐步收口为可评审、可共享的 PRD 交付物，并在需要时追加原型、原型样式统一、规则稿和流程图。

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
        ├── write-prd/
        ├── build-prototype/
        ├── style-prototype/
        ├── write-rules/
        ├── make-flowchart/
        └── shared/
```

## 安装

推荐通过 Codex 自带的 `skill-installer` 从 GitHub 安装这个 skill。

如果仓库 owner 是 `whauff`，仓库名是 `ai-prd-workflow`，安装命令示例为：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo whauff/ai-prd-workflow \
  --path skills/ai-prd-workflow
```

安装完成后，重启 Codex 以识别新 skill。

## 适用场景

- 需求还比较散，需要先澄清
- 已有材料较多，需要收口成 PRD
- 页面和交互容易引起分歧，需要原型
- 团队希望统一原型样式交付标准
- 规则口径或流程分支需要单独沉淀

## 文档

- [使用说明](docs/USAGE.md)
- [调用速查表](docs/CHEATSHEET.md)
- [调用示例](docs/EXAMPLES.md)
- [原型样式说明](docs/STYLE_GUIDE.md)
