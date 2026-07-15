---
layout: nijida-topic
title: GitHubにODTSをセットアップする
kicker: リファレンス実装
excerpt: 組織共通のIssueタイプとフィールドを、RepositoryテンプレートとProjectテンプレートに組み合わせます。
lang: ja
nav_id: projects
local_nav_id: installation
permalink: /ja/setup/
translations: { de: /de/einrichtung/, en: /en/setup/, ja: /ja/setup/ }
---

## 構成要素

1. 組織は`ODTS EPIC`、`ODTS ITEM`、`ODTS TASK`をネイティブIssueタイプとして用意します。
2. 各階層のサブタイプは、組織共通の単一選択フィールドで提供します。
3. [ODTS-Specification Repositoryテンプレート](https://github.com/Nijida-Studio/ODTS-Specification)は、Issue Formsとすぐ使える基本構成を提供します。
4. ODTS-Specification Projectテンプレートは、ビューと最小限のステータス自動化を提供します。

Repositoryテンプレートには、新しいプロジェクトが削除しなければならないODTS説明文を意図的に含めません。文書は`ODTS-Home`に置かれます。

## コピーした後

GitHubはProjectテンプレートからAuto-addワークフローをコピーしないため、対象Repositoryごとに設定します。その後、親子関係とサブタイプを持つEpic、Item、Taskを1つずつ作って検証します。

完全な手順は[インストールガイド](https://github.com/Nijida-Studio/ODTS-Home/blob/main/INSTALLATION.md)にあります。
