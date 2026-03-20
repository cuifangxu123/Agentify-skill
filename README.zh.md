**[简体中文](README.zh.md)** · [English](README.md) · [日本語](README.ja.md)

# Agentify

让网页与站点更容易被 **AI 智能体**、**爬虫**与**自动化工具**理解、导航和操作：分析可代理性、改写模板、输出团队可用的设计规范。

## 功能概览

| 能力 | 说明 |
|------|------|
| **Analyze** | 按 9 个维度（语义 HTML、ARIA、结构化数据、表单、导航、`data-testid`、选择器稳定性、API 可发现性、Meta 等）打分（0–100），并给出可执行的改进建议。 |
| **Rewrite** | 在**不破坏现有行为与外观**的前提下，为 HTML/JSX/Vue/Svelte 等补充语义、ARIA、`data-testid`、JSON-LD、无障碍与可自动化属性。 |
| **Design Spec** | 基于项目技术栈生成 `agent-friendly-spec.md` 级别的设计规范（含优先级、示例、反模式与验证方式）。 |

触发场景示例：*agent-friendly*、*改进 SEO / 结构化数据*、*加 data-testid*、*爬虫友好*、*a11y 审计* 等。

## 仓库结构

```
Agentify/
├── README.md               # English（仓库默认）
├── README.zh.md
├── README.ja.md
├── agentify.skill          # 预打包技能（若你的环境支持从该格式导入）
└── agentify/               # 技能源码（Cursor / Claude 等 Agent Skills）
    ├── SKILL.md            # 技能入口与工作流程
    └── references/         # 评分、清单、模式、框架说明、规范模板等
```

详细能力与流程以 [`agentify/SKILL.md`](agentify/SKILL.md) 为准。

## 使用方式

1. **作为 Agent Skill**  
   将 `agentify` 目录放到你所用工具要求的 Skills 目录中（例如 Cursor 的 user skills 路径），确保能加载其中的 `SKILL.md` 与 `references/`。

2. **预打包文件**  
   若编辑器或 CLI 支持 `.skill` 格式，可直接使用根目录下的 `agentify.skill` 导入（具体步骤以对应产品文档为准）。

## 许可

未在仓库中声明许可证时，默认保留所有权利；如需开源分发，请自行补充 `LICENSE` 文件。
