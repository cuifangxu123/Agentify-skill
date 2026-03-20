[简体中文](README.zh.md) · **[English](README.md)** · [日本語](README.ja.md)

# Agentify

Help web pages and sites be easier for **AI agents**, **crawlers**, and **automation tools** to understand, navigate, and operate: analyze agent-friendliness, rewrite templates, and produce team-ready design specs.

## Features

| Capability | Description |
|------------|-------------|
| **Analyze** | Score (0–100) across 9 areas (semantic HTML, ARIA, structured data, forms, navigation, `data-testid`, selector stability, API discoverability, meta signals) with actionable recommendations. |
| **Rewrite** | Enrich HTML/JSX/Vue/Svelte with semantics, ARIA, `data-testid`, JSON-LD, and accessibility/automation attributes **without changing behavior or visuals**. |
| **Design Spec** | Generate an `agent-friendly-spec.md`-style specification for your stack (priorities, examples, anti-patterns, verification). |

Example triggers: *agent-friendly*, *SEO / structured data*, *add data-testid*, *scraper-friendly*, *a11y audit*, etc.

## Repository layout

```
Agentify/
├── README.md               # English (default)
├── README.zh.md
├── README.ja.md
├── agentify.skill          # Packaged skill (if your tool supports this format)
└── agentify/               # Skill source (Cursor / Claude Agent Skills, etc.)
    ├── SKILL.md            # Entry point and workflows
    └── references/         # Scoring, checklists, patterns, frameworks, spec templates
```

For full behavior, see [`agentify/SKILL.md`](agentify/SKILL.md).

## Usage

1. **As an Agent Skill**  
   Place the `agentify` folder in your tool’s Skills directory (e.g. Cursor user skills) so `SKILL.md` and `references/` load correctly.

2. **Packaged file**  
   If your editor or CLI supports `.skill`, import `agentify.skill` from the repo root (follow that product’s docs).

## License

If no `LICENSE` is present, all rights are reserved; add a `LICENSE` file before open distribution.
