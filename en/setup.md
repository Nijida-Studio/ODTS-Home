---
layout: nijida-topic
title: Set up ODTS on GitHub
kicker: Reference implementation
excerpt: Organization-wide types and fields combine with one repository template and one Project template.
lang: en
nav_id: projects
local_nav_id: installation
permalink: /en/setup/
translations: { de: /de/einrichtung/, en: /en/setup/, ja: /ja/setup/ }
---

## Components

1. The organization provides `ODTS EPIC`, `ODTS ITEM`, and `ODTS TASK` as native issue types.
2. One organization-wide single-select field provides the subtypes for each level.
3. The [ODTS-Specification repository template](https://github.com/Nijida-Studio/ODTS-Specification) supplies Issue Forms and immediately reusable base configuration.
4. The ODTS-Specification Project template supplies views and minimal status automation.

The repository template intentionally contains no ODTS explanation that a new project would first have to delete. Documentation remains here in `ODTS-Home`.

## Versions

`.github/odts.yml` declares the current ODTS version of a repository. Every new Epic, Item, and Task carries that version as a visible `ODTS Version` value in the Issue body. When a repository is updated, existing Issues retain their original version; only new or explicitly migrated Issues use the new version.

An optional repository Custom Property named `ODTS Status` can provide visible feedback from Souran or other tooling to administrators. It is not configuration or a source of truth. GitHub Projects do not receive an ODTS version because they are only views that may combine Issues from different repositories and historical periods.

## After copying

Auto-add must be configured for every target repository because GitHub does not copy that workflow from a Project template. Validate the installation with one Epic, Item, and Task, including parent relationships, subtypes, and the version value stored in each Issue body.

The [installation guide](https://github.com/Nijida-Studio/ODTS-Home/blob/main/INSTALLATION.md) contains the complete procedure.
