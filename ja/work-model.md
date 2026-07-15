---
layout: nijida-topic
title: ODTSの作業モデル
kicker: 3つの階層、明確な役割
excerpt: 作業をEpic → Item → Taskに分け、それぞれの階層が異なる問いに答えます。
lang: ja
nav_id: projects
local_nav_id: model
permalink: /ja/work-model/
translations: { de: /de/arbeitsmodell/, en: /en/work-model/, ja: /ja/work-model/ }
---

## 階層

**ODTS EPIC**は、戦略目標、ワークフロー目標、アーキテクチャ方針、または要件を表します。

**ODTS ITEM**は、まとまりのある実装領域を表し、必ず1つの親Epicを持ちます。

**ODTS TASK**は、実行可能な作業単位を表し、必ず1つの親Itemを持ちます。

```text
ODTS EPIC
└── ODTS ITEM
    └── ODTS TASK
```

## サブタイプ

- Epic: `UserStory`, `Requirement`
- Item: `Feature`, `FeatureRequest`, `Bug`, `Documentation`, `Test`
- Task: `Work`, `ToDo`

サブタイプは意味を詳しくしますが、Issueタイプを置き換えません。意味のある保留作業は、ソースコードのコメントだけに残さず`ToDo` Taskとして記録します。

## 意図的に規定しないもの

優先度、工数、開始日、目標日は任意のチームフィールドです。ラベルはRepository固有の補足情報に使えますが、構造的なタイプ、サブタイプ、ステータスを重複させてはいけません。
