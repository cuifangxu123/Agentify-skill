[简体中文](README.zh.md) · [English](README.md) · **[日本語](README.ja.md)**

# Agentify

Web ページやサイトを **AI エージェント**、**クローラ**、**自動化ツール**が理解・操作しやすくするためのスキルです。エージェント適性の分析、テンプレートの書き換え、チーム向け設計仕様の生成に対応します。

## 機能概要

| 機能 | 説明 |
|------|------|
| **Analyze** | 9 分野（セマンティック HTML、ARIA、構造化データ、フォーム、ナビゲーション、`data-testid`、セレクタの安定性、API の発見しやすさ、メタ情報など）を 0–100 点で評価し、実行可能な改善案を提示します。 |
| **Rewrite** | **既存の挙動や見た目を変えずに**、HTML/JSX/Vue/Svelte へセマンティクス、ARIA、`data-testid`、JSON-LD、アクセシビリティ／自動化向け属性を追加します。 |
| **Design Spec** | プロジェクトの技術スタックに合わせ、`agent-friendly-spec.md` 相当の設計仕様（優先度、例、アンチパターン、検証方法）を生成します。 |

想定トリガー例：*agent-friendly*、*SEO / 構造化データ*、*data-testid を追加*、*スクレイピング向け*、*a11y 監査* など。

## リポジトリ構成

```
Agentify/
├── README.md               # English（既定）
├── README.zh.md
├── README.ja.md
├── agentify.skill          # パッケージ済みスキル（対応ツール向け）
└── agentify/               # スキル本体（Cursor / Claude などの Agent Skills）
    ├── SKILL.md            # エントリとワークフロー
    └── references/         # 採点、チェックリスト、パターン、フレームワーク、仕様テンプレート
```

詳細は [`agentify/SKILL.md`](agentify/SKILL.md) を参照してください。

## 使い方

1. **Agent Skill として**  
   `agentify` フォルダを、利用ツールが指定する Skills ディレクトリ（例：Cursor の user skills）に配置し、`SKILL.md` と `references/` が読み込まれるようにします。

2. **パッケージファイル**  
   エディタや CLI が `.skill` に対応している場合、リポジトリ直下の `agentify.skill` をインポートします（手順は各製品のドキュメントに従ってください）。

## ライセンス

`LICENSE` がない場合、著作権は留保されます。公開配布する前に `LICENSE` を追加してください。
