---
layout: nijida-topic
title: The ODTS work model
kicker: Three levels, clear responsibility
excerpt: Work is arranged as Epic → Item → Task. Each level answers a different question.
lang: en
nav_id: projects
local_nav_id: model
permalink: /en/work-model/
translations: { de: /de/arbeitsmodell/, en: /en/work-model/, ja: /ja/work-model/ }
---

## Hierarchy

An **ODTS EPIC** describes a strategic goal, workflow objective, architectural direction, or requirement.

An **ODTS ITEM** groups a coherent implementation area and has exactly one parent Epic.

An **ODTS TASK** is an actionable unit of work and has exactly one parent Item.

```text
ODTS EPIC
└── ODTS ITEM
    └── ODTS TASK
```

## Subtypes

- Epic: `UserStory`, `Requirement`
- Item: `Feature`, `FeatureRequest`, `Bug`, `Documentation`, `Test`
- Task: `Work`, `ToDo`

Subtypes refine meaning; they do not replace issue types. Meaningful deferred work becomes a `ToDo` Task instead of surviving only as a source-code comment.

## Deliberately left open

Priority, effort, start date, and target date are optional team fields. Labels may add repository context but must not duplicate structural types, subtypes, or status.
