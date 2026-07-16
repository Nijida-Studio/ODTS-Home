---
layout: nijida-knowledge-home
title: ODTS
kicker: オープンな開発・タスク構造
excerpt: アイデアから追跡可能なIssue、文書、テスト、実装まで、計画可能な作業のための小さなリファレンスです。
lang: ja
nav_id: projects
local_nav_id: overview
permalink: /ja/
translations: { de: /de/, en: /en/, ja: /ja/ }
knowledge_sections:
  - title: ODTSを知る
    excerpt: モデルから実際の利用まで、3つの短い入口を用意しています。
    items:
      - { title: 作業モデル, text: "Epic、Item、Taskが小さく明確な階層を作ります。", url: /ja/work-model/ }
      - { title: 作業手順, text: "完全な実装より前に骨格、基本文書、テストを作ります。", url: /ja/workflow/ }
      - { title: GitHubセットアップ, text: "2つのテンプレートと組織共通フィールドがリファレンス実装を構成します。", url: /ja/setup/ }
---

ODTSは、チームが実装の前に作業を理解できる形で記述し、結果を追跡可能に保つための仕様です。規則は意図的に少なく、プログラミング言語、テストフレームワーク、リリースモデル、ブランチ戦略は指定しません。

> ODTSはソフトウェアではなく仕様です。GitHub構成は最初のリファレンス実装であり、ODTSそのものの定義ではありません。

> **文書の状態:** この読みやすい説明はODTS 1.0以前の開発状態を記述しています。常に[ODTS-Specification](https://github.com/Nijida-Studio/ODTS-Specification)が正式な基準です。その`main`ブランチは現在、未公開のODTS 1.0リリース候補です。この文書には現在の仕様との差異、誤り、古い内容が含まれる場合があります。
