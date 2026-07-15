---
layout: nijida-topic
title: Working with ODTS
kicker: Issue-first, documentation- and test-oriented
excerpt: The task, structure, intended behavior, and validation become visible before the complete logic is written.
lang: en
nav_id: projects
local_nav_id: workflow
permalink: /en/workflow/
translations: { de: /de/arbeitsweise/, en: /en/workflow/, ja: /ja/workflow/ }
---

## Normal sequence

1. Create and connect the Epic, Item, and Task.
2. Understand the selected Task together with its parent Item and Epic.
3. Create files, types, interfaces, and signatures as a skeleton.
4. Briefly document purpose, intended behavior, and relevant constraints.
5. Add tests for the intended behavior where technically possible.
6. Review that foundation.
7. Implement the behavior and keep issues, documentation, and tests synchronized.

If a test cannot reasonably precede implementation, the Task or pull request explains why and identifies an alternative validation method.

## Completion

A Task is complete only when its result or non-implementation outcome is documented, documentation is accurate, tests exist or an exception is explained, relevant follow-up work is tracked, and the required review is complete.

The detailed agreement is available in [Contributing with ODTS](https://github.com/Nijida-Studio/ODTS-Home/blob/main/CONTRIBUTING.md).
