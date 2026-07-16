# ODTS Documentation Snapshot

> [!IMPORTANT]
> This document is a human-readable documentation snapshot of a pre-1.0 ODTS development state. It is not authoritative. The authoritative source is always [`ODTS-Specification`](https://github.com/Nijida-Studio/ODTS-Specification). Its `main` branch is currently the unreleased ODTS 1.0 release candidate. This document may contain differences, errors, or older artifacts.

ODTS is a narrow reference framework for agile project management. It is designed primarily for software development, while its planning model can also be used for other kinds of projects.

Its central purpose is to help developers produce maintainable documentation and tests as part of implementation work—not as optional cleanup after the code is finished.

This document is maintained in ODTS-Home as a human-readable description. The authoritative behavior is defined by the **ODTS-Specification** GitHub repository template and the associated **ODTS-Specification** GitHub Project template.

## 1. Scope

ODTS defines:

- an issue-first planning workflow;
- a three-level issue hierarchy;
- subtypes for each hierarchy level;
- optional team-defined planning fields;
- a documentation-and-test-first implementation workflow;
- a GitHub reference mapping for issue types, issue fields, labels, repository templates, and Project templates.

ODTS does not prescribe a programming language, test framework, release model, branching strategy, or complete set of repository labels.

## 2. Normative language

The terms **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** describe requirement levels.

- **MUST** and **MUST NOT** are mandatory.
- **SHOULD** and **SHOULD NOT** are recommended unless a documented reason justifies an exception.
- **MAY** is optional.

## 3. Core workflow

Work MUST be described by issues before it is implemented.

For software development, the normal sequence is:

1. Create and structure the necessary Epic, Item, and Task issues.
2. Select a Task and understand its Parent Item and Epic.
3. Create the implementation skeleton before writing the implementation logic.
4. Add rudimentary code documentation to that skeleton.
5. Add tests that describe the intended behavior before implementation, where technically possible.
6. Review the skeleton, documentation, and tests.
7. Implement the behavior.
8. Keep issues, documentation, and tests synchronized with the implementation.
9. Complete the Task only after implementation, documentation, tests, and traceability are acceptable.

For a Swift change, for example, step 3 can mean creating the target file, type declarations, public signatures, and documented placeholders before filling in method bodies.

If a test cannot reasonably be written before implementation, the Task or pull request MUST explain why and identify the alternative validation method.

## 4. Issue model

ODTS uses the following hierarchy:

```text
Epic
└── Item
    └── Task
```

An **Epic** describes a strategic goal, workflow goal, architectural direction, or requirement.

An **Item** describes a coherent implementation area. Every Item MUST have exactly one Parent Epic.

A **Task** describes an actionable unit of work. Every Task MUST have exactly one Parent Item.

GitHub parent/sub-issue relationships SHOULD represent this hierarchy. Related issues MAY be linked without changing the hierarchy.

## 5. Subtypes

Subtypes refine the meaning of an issue. They do not replace the organization issue types ODTS EPIC, ODTS ITEM, and ODTS TASK.

### 5.1 Epic subtypes

- **UserStory** — a user-, workflow-, or process-oriented goal.
- **Requirement** — an external constraint, prerequisite, or mandatory condition.

### 5.2 Item subtypes

- **Feature** — planned functionality or an implementation area.
- **FeatureRequest** — a requested extension or improvement.
- **Bug** — incorrect behavior that requires correction.
- **Documentation** — user-facing, integration, architectural, or operational documentation work.
- **Test** — validation or testing work that is substantial enough to be managed as its own Item.

### 5.3 Task subtypes

- **Work** — active implementation, documentation, testing, refactoring, automation, or other concrete work.
- **ToDo** — intentionally deferred work, technical debt, cleanup, or a future improvement.

Meaningful deferred work SHOULD be recorded as a ToDo Task instead of remaining only as a source-code comment.

## 6. Optional team planning fields

Priority, Effort, Start date, and Target date are general planning fields, not part of the ODTS core. An organization MAY provide them as organization-wide issue fields, while each team decides whether and how to use them.

### Priority

The meaning and options of Priority are chosen by the organization or team. One possible model is the [Eisenhower Matrix](https://www.eisenhower.me/eisenhower-matrix/), which evaluates work by urgency and importance. A team MAY represent it as:

- **A** — important and urgent;
- **B** — important, not urgent;
- **C** — urgent, less important;
- **P** — neither important nor urgent; Papierkorb.

Teams MAY instead use another priority model. Priority expresses a team's scheduling judgment and MUST NOT change the structural meaning of an ODTS issue.

### Effort and dates

- **Effort** MAY express a team's estimate of the work involved.
- **Start date** MAY express when work is intended to begin.
- **Target date** MAY express when a result is intended to be reached.

These fields are optional team extensions. Their definitions, scales, and working agreements belong to the team or organization using them.

### Visibility

For each organization issue field, the organization chooses **Public** or **Organization only** visibility independently. Public fields can be shown to everyone where GitHub permits it. Organization-only fields are limited to organization members and authorized repository collaborators. ODTS does not prescribe one visibility setting.

## 7. Labels

Labels provide quickly visible, repository-specific supplementary information. They MUST NOT duplicate the structural meaning of issue types, subtypes, priority, or status.

The reference labels are:

- `help wanted`
- `question`
- `needs review`
- `bootstrap`
- `blocked`
- `migration`

Each repository SHOULD keep only the labels useful for that repository and MAY add domain-specific labels. Labels are configured per repository, not per GitHub Project.

## 8. Documentation- and test-first development

Before the main implementation begins, a developer SHOULD create:

- the required files and directories;
- types, protocols, interfaces, modules, components, and signatures;
- short documentation describing purpose, intended behavior, and relevant constraints;
- tests for the intended behavior, where technically possible.

Documentation SHOULD identify the relevant Item and Task when that relationship would otherwise be difficult to reconstruct. It SHOULD explain why the code exists and what is intentionally still missing. It SHOULD NOT add issue metadata to every line or repeat information that is already obvious from the code.

Tests SHOULD state the behavior future developers must preserve. Tests may initially fail because the implementation does not yet exist.

A pull request SHOULD make the two stages visible:

1. skeleton, documentation, and tests;
2. implementation and final verification.

The stages MAY occur in one pull request. A separate preliminary pull request is optional.

## 9. GitHub reference implementation

ODTS itself is independent of a specific tool. Its first reference implementation uses GitHub.

### 9.1 Organization-wide issue types

The organization MUST provide these GitHub issue types:

- **ODTS EPIC**
- **ODTS ITEM**
- **ODTS TASK**

They are configured in the organization settings under **Planning → Issue types**.

### 9.2 Organization-wide issue fields

The organization MUST provide these single-select issue fields:

| Issue field | Options | Pinned to issue type |
| --- | --- | --- |
| `ODTS Epic Subtype` | `UserStory`, `Requirement` | ODTS EPIC |
| `ODTS Item Subtype` | `Feature`, `FeatureRequest`, `Bug`, `Documentation`, `Test` | ODTS ITEM |
| `ODTS Task Subtype` | `Work`, `ToDo` | ODTS TASK |

These fields are configured in the organization settings under **Planning → Issue fields**. Subtype fields MUST be pinned only to their corresponding issue type.

Issue fields are the source of truth. ODTS templates MUST NOT duplicate them as dropdowns in the issue body. Optional organization fields such as Priority, Effort, Start date, and Target date MAY be added according to team needs.

### 9.3 Repository configuration

Each participating repository SHOULD:

- originate from the ODTS repository template;
- enable Issues;
- keep compact Epic, Item, and Task issue forms;
- adapt its labels at repository level;
- use the native issue type and issue field controls provided by GitHub.

### 9.4 Project configuration

The GitHub Project **ODTS-Specification** is the reference Project template. A project created from it SHOULD provide shared views and workflows, while organization issue fields remain the source of truth for ODTS subtypes and any optional team planning fields.

Project-level custom fields MUST NOT duplicate the organization issue fields with the same meaning.

The reference Project template SHOULD provide these status workflows:

- when an item is added, set Status to `New`;
- when an Issue is closed, set Status to `Done`.

Transitions to `In Progress` and `Stasis` SHOULD remain deliberate manual decisions. A reopened Issue SHOULD be reassessed manually because its correct status may be `New`, `In Progress`, or `Stasis`.

Auto-add MUST be configured for the target repository after creating a Project from the template because GitHub does not copy Auto-add workflows. Auto-archive SHOULD remain disabled by default so completed history stays visible in the `All` view.

## 10. Traceability and completion

Commits and pull requests SHOULD reference the Task they implement. A change SHOULD remain traceable to one Parent Item; work crossing multiple Parent Items SHOULD be split where practical.

A Task is complete only when:

- the requested behavior is implemented or the non-implementation outcome is documented;
- documentation is present and accurate;
- tests exist where technically possible, or the exception is documented;
- deferred work is represented by issues where meaningful;
- the result has been reviewed to the level required by the project.

## 11. Reference repositories

- [ODTS-Home](https://github.com/Nijida-Studio/ODTS-Home) — normative description, user documentation, contribution workflow, and installation guide.
- [ODTS-Specification](https://github.com/Nijida-Studio/ODTS-Specification) — bare prepared reference implementation and repository template.
