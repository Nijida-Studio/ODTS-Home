---
layout: nijida-topic
title: Das ODTS-Arbeitsmodell
kicker: Drei Ebenen, klare Verantwortung
excerpt: Arbeit wird als Epic → Item → Task gegliedert. Jede Ebene beantwortet eine andere Frage.
lang: de
nav_id: projects
local_nav_id: model
permalink: /de/arbeitsmodell/
translations:
  de: /de/arbeitsmodell/
  en: /en/work-model/
  ja: /ja/work-model/
---

## Hierarchie

**ODTS EPIC** beschreibt ein strategisches Ziel, ein Workflow-Ziel, eine architektonische Richtung oder eine Anforderung.

**ODTS ITEM** bündelt einen zusammenhängenden Umsetzungsbereich und besitzt genau ein übergeordnetes Epic.

**ODTS TASK** ist eine ausführbare Arbeitseinheit und besitzt genau ein übergeordnetes Item.

```text
ODTS EPIC
└── ODTS ITEM
    └── ODTS TASK
```

## Subtypen

- Epic: `UserStory`, `Requirement`
- Item: `Feature`, `FeatureRequest`, `Bug`, `Documentation`, `Test`
- Task: `Work`, `ToDo`

Subtypen verfeinern die Bedeutung. Sie ersetzen nicht den Issue-Typ. Sinnvoll aufgeschobene Arbeit wird als `ToDo`-Task erfasst, statt nur als Kommentar im Quelltext zu verschwinden.

## Was bewusst offenbleibt

Priorität, Aufwand sowie Start- und Zieldatum sind optionale Teamfelder. Labels dürfen ergänzenden Repository-Kontext geben, aber die strukturellen Typen, Subtypen oder Statuswerte nicht duplizieren.
