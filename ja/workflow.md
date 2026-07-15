---
layout: nijida-topic
title: ODTSで作業する
kicker: Issueを先に、文書とテストを重視
excerpt: 完全なロジックを書く前に、タスク、構造、意図する動作、検証方法を見える形にします。
lang: ja
nav_id: projects
local_nav_id: workflow
permalink: /ja/workflow/
translations: { de: /de/arbeitsweise/, en: /en/workflow/, ja: /ja/workflow/ }
---

## 基本の手順

1. Epic、Item、Taskを作成し、親子関係を設定します。
2. 選択したTaskを、その親ItemとEpicとともに理解します。
3. ファイル、型、インターフェース、シグネチャを骨格として作ります。
4. 目的、意図する動作、重要な制約を短く文書化します。
5. 技術的に可能な場合、意図する動作のテストを作ります。
6. この基礎をレビューします。
7. 動作を実装し、Issue、文書、テストを同期させます。

実装前にテストを書くことが合理的でない場合は、TaskまたはPull Requestに理由と代替の検証方法を記載します。

## 完了条件

結果または実装しない判断が記録され、文書が正確で、テストが存在するか例外が説明され、重要な後続作業がIssue化され、必要なレビューが終わった時にTaskは完了します。

詳細は[Contributing with ODTS](https://github.com/Nijida-Studio/ODTS-Home/blob/main/CONTRIBUTING.md)にあります。
