---
layout: nijida-topic
title: ODTS auf GitHub einrichten
kicker: Referenzumsetzung
excerpt: Organisationsweite Typen und Felder werden mit einer Repository- und einer Project-Vorlage kombiniert.
lang: de
nav_id: projects
local_nav_id: installation
permalink: /de/einrichtung/
translations:
  de: /de/einrichtung/
  en: /en/setup/
  ja: /ja/setup/
---

## Die Bausteine

1. Die Organisation stellt `ODTS EPIC`, `ODTS ITEM` und `ODTS TASK` als native Issue-Typen bereit.
2. Je ein organisationsweites Auswahlfeld enthält die Subtypen der zugehörigen Ebene.
3. Die [ODTS-Specification Repository-Vorlage](https://github.com/Nijida-Studio/ODTS-Specification) liefert Issue Forms und eine sofort nutzbare Grundkonfiguration.
4. Die ODTS-Specification Project-Vorlage liefert Ansichten und minimale Statusautomatisierung.

Die Repository-Vorlage ist absichtlich leer von ODTS-Erklärtexten, die ein neues Projekt erst löschen müsste. Die Dokumentation bleibt hier in `ODTS-Home`.

## Nach dem Kopieren

Auto-add muss für jedes Ziel-Repository neu eingerichtet werden, weil GitHub diesen Workflow nicht aus einer Project-Vorlage übernimmt. Danach wird die Installation mit je einem Epic, Item und Task samt Elternbeziehungen und Subtypen geprüft.

Die vollständige Schrittfolge enthält die [Installationsanleitung](https://github.com/Nijida-Studio/ODTS-Home/blob/main/INSTALLATION.md).
