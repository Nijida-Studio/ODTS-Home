# Note 5月 19, 2026 14:41:54 #
# ODTS 1.0 Beta Documentation

## Table of Contents

- [1. Introduction](#1-introduction)
- [2. What Is ODTS?](#2-what-is-odts)
- [3. Core Philosophy](#3-core-philosophy)
- [4. Self-Hosting And Bootstrap Philosophy](#4-self-hosting-and-bootstrap-philosophy)
- [5. Core Terminology](#5-core-terminology)
  - [5.1 Epic](#51-epic)
  - [5.2 Item](#52-item)
  - [5.3 Task](#53-task)
  - [5.4 Parent Relationships](#54-parent-relationships)
  - [5.5 Related Relationships](#55-related-relationships)
  - [5.6 Domains](#56-domains)
- [6. Developer Roles](#6-developer-roles)
  - [6.1 Origin Developer](#61-origin-developer)
  - [6.2 User Developer](#62-user-developer)
  - [6.3 Workflow Reviewer](#63-workflow-reviewer)
- [7. ODTS Workflow Structure](#7-odts-workflow-structure)
  - [7.1 Workflow Hierarchy](#71-workflow-hierarchy)
  - [7.2 Metadata Philosophy](#72-metadata-philosophy)
  - [7.3 GitHub Project Integration](#73-github-project-integration)
- [8. Epic Types](#8-epic-types)
  - [8.1 UserStory](#81-userstory)
  - [8.2 Requirement](#82-requirement)
- [9. Item Types](#9-item-types)
  - [9.1 Feature](#91-feature)
  - [9.2 FeatureRequest](#92-featurerequest)
  - [9.3 Bug](#93-bug)
  - [9.4 Documentation](#94-documentation)
  - [9.5 Test](#95-test)
- [10. Task Types](#10-task-types)
  - [10.1 Work](#101-work)
  - [10.2 ToDo](#102-todo)
- [11. Workflow States](#11-workflow-states)
  - [11.1 New](#111-new)
  - [11.2 Stasis](#112-stasis)
  - [11.3 In Progress](#113-in-progress)
  - [11.4 Done](#114-done)
- [12. Views And Workflow Organization](#12-views-and-workflow-organization)
  - [12.1 Backlog](#121-backlog)
  - [12.2 Work](#122-work)
  - [12.3 My View](#123-my-view)
  - [12.4 All Views](#124-all-views)
- [13. Labels Philosophy](#13-labels-philosophy)
- [14. Commit Philosophy](#14-commit-philosophy)
- [15. Why ODTS Uses GitHub Projects](#15-why-odts-uses-github-projects)
- [16. Known GitHub Limitations](#16-known-github-limitations)
- [17. ODTS 1.0 Beta Status](#17-odts-10-beta-status)
- [18. Developer Implementation Workflow](#18-developer-implementation-workflow)
- [19. Future Evolution](#19-future-evolution)

---

# 1. Introduction

ODTS (Origin Development Tracking System) is a workflow-oriented project organization and development tracking system built on top of GitHub Issues and GitHub Projects.

ODTS focuses on:
- traceability
- workflow clarity
- self-hosting development
- long-term maintainability
- reusable workflow structures
- architecture-oriented organization

Unlike many traditional issue tracking systems, ODTS intentionally separates:
- structural workflow semantics
- implementation workflows
- communication metadata
- organizational metadata

ODTS is designed to evolve together with the systems developed through it.

---

# 2. What Is ODTS?

ODTS is both:
- a workflow philosophy
- and a practical GitHub-based workflow implementation.

The system was designed to:
- organize long-term development structures
- separate strategic and operational work
- improve traceability
- support reusable workflows
- support self-hosted system evolution
- allow architecture-oriented development tracking

ODTS intentionally uses GitHub as infrastructure instead of replacing it.

GitHub provides:
- repositories
- issues
- pull requests
- projects
- version control

ODTS adds:
- workflow semantics
- hierarchy structure
- metadata structure
- organizational conventions
- reusable templates
- project workflow organization

---

# 3. Core Philosophy

ODTS follows several core design principles:

## Reusable Structure

Workflow structures should be reusable and reproducible.

## Minimal Semantic Ambiguity

Every structural object should have a clearly defined purpose.

## Workflow Transparency

Development progress and workflow state should remain understandable over long periods of time.

## Architecture Orientation

ODTS focuses strongly on long-term maintainability and architectural clarity.

## Self-Hosting

ODTS develops itself using ODTS.

---

# 4. Self-Hosting And Bootstrap Philosophy

ODTS was developed through an explicit bootstrap process.

The bootstrap phase intentionally separated:
- experimental workflow evolution
- stable workflow structures

This was achieved through:
- a dedicated `bootstrap` branch
- reusable workflow templates
- iterative workflow evolution
- self-hosted development

The bootstrap process remained preserved historically to maintain complete workflow traceability.

ODTS now exists as a reusable self-hosting workflow system.

---

# 5. Core Terminology

## 5.1 Epic

Epics describe:
- strategic goals
- workflow goals
- architectural goals
- long-term implementation directions
- requirements

Epics are intentionally domain-independent.

A single Epic may require implementation work across multiple Domains.

---

## 5.2 Item

Items describe:
- concrete implementation areas
- functional implementation units
- architecture work
- documentation work
- testing work

Items always belong to exactly one Parent Epic.

Items always belong to a specific Domain.

---

## 5.3 Task

Tasks describe:
- concrete work units
- operational implementation steps
- actionable development work

Tasks always belong to exactly one Parent Item.

Tasks normally inherit the Domain of their Parent Item.

---

## 5.4 Parent Relationships

Parent relationships describe structural hierarchy.

Examples:
- Item → Parent Epic
- Task → Parent Item

Parent relationships define workflow structure.

---

## 5.5 Related Relationships

Related relationships describe contextual relationships without creating structural hierarchy.

Examples:
- architecture dependencies
- workflow dependencies
- migration relationships
- implementation relationships
- historical bootstrap relationships

---

## 5.6 Domains

Domains describe concrete implementation areas.

Domains are used for:
- Items
- optionally Tasks

Domains are intentionally not used for Epics.

Examples:
- Architecture
- Documentation
- Testing
- UI
- Backend

---

# 6. Developer Roles

## 6.1 Origin Developer

An Origin Developer works on the origin-level infrastructure of a software ecosystem.

The term does not specifically refer to ODTS itself.

Instead, it describes developers who work on foundational systems that are used by other software.

Examples:
- operating systems
- compilers
- runtime environments
- shared libraries
- infrastructure frameworks
- foundational APIs

Example:

A developer working on the GNU C Library (glibc) is an Origin Developer.

A developer building an application that uses glibc is a User Developer.

Within ODTS, the term "Origin" always refers to the developer of the software currently managed through ODTS.

This means:
- developers working on the managed system itself are Origin Developers
- developers building software on top of that system are User Developers

Origin Developers are primarily responsible for:
- architecture
- maintainability
- infrastructure integrity
- long-term compatibility
- workflow evolution
- structural consistency

---

## 6.2 User Developer

User Developers primarily work with the externally visible functionality of a system.

User Developers focus more strongly on:
- feature usage
- external APIs
- user-facing workflows
- practical implementation usage

---

## 6.3 Workflow Reviewer

The Workflow Reviewer is responsible for reviewing workflow correctness and process consistency.

This may include:
- workflow validation
- review approval
- architecture review
- documentation review
- process review
- traceability review

The Workflow Reviewer role intentionally remains broader than traditional code review.

---

# 7. ODTS Workflow Structure

## 7.1 Workflow Hierarchy

ODTS uses a three-level hierarchy:

```text
Epic
└── Item
    └── Task
```

This hierarchy separates:
- strategic planning
- implementation organization
- operational work

---

## 7.2 Metadata Philosophy

ODTS separates:
- structural metadata
- workflow metadata
- communication metadata

Structural metadata belongs to ODTS fields.

Communication and contextual metadata may additionally use GitHub Labels.

---

## 7.3 GitHub Project Integration

ODTS uses GitHub Projects as the primary workflow organization layer.

Repositories primarily contain:
- code
- files
- templates
- version history

Projects primarily contain:
- workflow organization
- metadata
- workflow views
- status organization
- review organization

---

# 8. Epic Types

## 8.1 UserStory

UserStory Epics describe:
- workflow goals
- user-oriented workflows
- development workflows
- organizational goals

---

## 8.2 Requirement

Requirement Epics describe:
- technical constraints
- external requirements
- implementation prerequisites
- mandatory system conditions

Requirements exist independently from workflow preferences.

---

# 9. Item Types

## 9.1 Feature

Feature Items describe planned implementation functionality.

---

## 9.2 FeatureRequest

FeatureRequest Items describe requested functionality extensions or improvements.

---

## 9.3 Bug

Bug Items describe incorrect behavior that requires correction.

---

## 9.4 Documentation

Documentation Items describe work related to external or user-facing documentation structures.

Examples:
- user documentation
- setup guides
- architecture handbooks
- deployment documentation
- tutorials
- public specifications

Internal workflow traceability and structural development history are intentionally handled through the ODTS workflow system itself.

---

## 9.5 Test

Test Items describe implementation work related to validation and testing.

---

# 10. Task Types

## 10.1 Work

Work Tasks describe actively implemented development work.

Examples:
- implementation
- refactoring
- testing
- workflow setup
- automation
- documentation implementation

---

## 10.2 ToDo

ToDo Tasks describe:
- deferred work
- postponed improvements
- future cleanup
- technical debt
- intentionally delayed implementation

A ToDo does not necessarily represent unfinished implementation quality.

---

# 11. Workflow States

## 11.1 New

The object exists but has not yet entered active workflow movement.

---

## 11.2 Stasis

The object intentionally remains inactive.

Stasis may represent:
- deferred work
- waiting states
- architectural pauses
- temporary inactivity
- external dependency waiting

Stasis intentionally remains semantically neutral.

---

## 11.3 In Progress

The object currently receives active workflow movement and implementation work.

---

## 11.4 Done

The workflow work for this object has ended.

Done intentionally does not imply:
- success
- failure
- deployment
- cancellation

Additional context may be documented through:
- comments
- notes
- related objects
- commits
- pull requests

---

# 12. Views And Workflow Organization

## 12.1 Backlog

The Backlog view focuses on:
- Epics
- Items
- strategic planning
- long-term workflow organization

Tasks are intentionally excluded.

---

## 12.2 Work

The Work view focuses on:
- operational implementation
- Items
- Tasks
- active implementation movement

Epics are intentionally excluded.

---

## 12.3 My View

My View focuses on:
- personally assigned work
- active workflow movement
- individual implementation responsibility

---

## 12.4 All Views

All views provide complete workflow visibility.

These views intentionally include:
- active objects
- inactive objects
- completed objects
- historical workflow structures

---

# 13. Labels Philosophy

ODTS intentionally separates:
- structural metadata
- from contextual communication metadata.

ODTS fields model:
- structure
- workflow semantics
- hierarchy
- status

Labels model:
- communication context
- temporary states
- additional hints
- workflow support information

Examples:
- help wanted
- question
- needs review
- bootstrap
- blocked
- migration

---

# 14. Commit Philosophy

ODTS uses strongly traceable commits.

Every meaningful commit should reference exactly one Parent Item.

Commit messages intentionally remain human-readable.

Example:

```text
Item #4
Task #5

Create initial ODTS Task template
```

Related relationships may additionally be documented.

---

# 15. Why ODTS Uses GitHub Projects

GitHub Projects provide:
- workflow visualization
- metadata organization
- views
- filters
- review organization
- workflow grouping

ODTS intentionally builds on top of GitHub instead of replacing it.

This keeps:
- infrastructure complexity low
- interoperability high
- workflow portability high

---

# 16. Known GitHub Limitations

GitHub Projects currently have several limitations.

Examples:
- limited hierarchical visualization
- limited field dependency support
- limited workflow automation
- limited relationship semantics
- inconsistent filtering behavior

ODTS intentionally works around these limitations through:
- metadata conventions
- workflow conventions
- reusable views
- reusable templates
- semantic separation

---

# 17. ODTS 1.0 Beta Status

ODTS 1.0 Beta represents the first fully self-hosting workflow version of ODTS.

ODTS 1.0 Beta already includes:
- reusable templates
- workflow structures
- project organization
- metadata systems
- status systems
- review concepts
- reusable project structures
- self-hosting workflow development

The bootstrap phase has been completed.

---

# 18. Developer Implementation Workflow

This section describes the recommended ODTS workflow from the perspective of an Origin Developer who implements a concrete Task.

The purpose of this workflow is to prevent undocumented code, missing tests, unclear ownership, and later reconstruction work.

ODTS assumes that implementation work should not begin with finished code. It should begin with structure, documentation, and tests.

---

## 18.1 Starting Point

A developer starts with an assigned Task.

The Task should belong to exactly one Parent Item.

Before implementation begins, the developer should understand:
- which Item the Task belongs to
- which Epic provides the larger context
- whether Related Items or Related Tasks exist
- whether a Workflow Reviewer is assigned
- which Domain the work belongs to

The assigned developer is the primary implementer.

The Workflow Reviewer is responsible for checking whether the ODTS workflow has been followed.

---

## 18.2 Create The Implementation Structure First

The first implementation step is not writing the finished code.

The developer first creates the structural code elements that are needed for the Task.

This may include:
- files
- directories
- classes
- structs
- interfaces
- protocols
- modules
- services
- components
- public APIs
- internal APIs
- placeholders for methods or functions

The goal is to create the shape of the implementation before the implementation logic exists.

---

## 18.3 Add Origin Developer Documentation To The Code

After creating the initial code structure, the developer adds Origin Developer documentation directly to the relevant code areas.

This documentation should explain:
- why this code structure exists
- which Parent Item it belongs to
- which Task introduces or changes it
- what the code is supposed to do
- what is intentionally not implemented yet
- which assumptions are being made
- which Related Items or Related Tasks matter

This documentation is not only explanatory text. It is part of the long-term traceability of the system.

Example:

```text
Parent Item: Item #...
Task: Task #...
Related Items: #...
Related Tasks: #...

Purpose:
This component provides the initial structure for ...

Implementation Notes:
The actual implementation is intentionally not completed in this stage.
```

The exact comment syntax may depend on the programming language.

In addition to Origin Developer documentation, User Developer documentation may also exist.

User Developer documentation includes:
- public APIs
- public workflows
- user-facing behavior
- integration usage
- setup instructions
- externally visible implementation behavior

ODTS intentionally distinguishes between:
- Origin Developer documentation
- User Developer documentation
- shared documentation intended for both groups

Origin Developer documentation focuses more strongly on:
- internal structure
- architecture
- traceability
- implementation reasoning
- workflow relationships
- internal implementation constraints

User Developer documentation focuses more strongly on:
- usage
- integration
- externally visible behavior
- setup
- practical consumption of the system

ODTS expects documentation areas to clearly indicate whether they are intended for:
- Origin Developers
- User Developers
- or both

The exact implementation method for this distinction may evolve in future ODTS versions.

---

---

## 18.4 Add Tests Before Implementation If Possible

After the structure and code documentation exist, the developer adds tests if this is technically possible.

The test may be:
- a unit test
- an integration test
- a snapshot test
- a UI test
- a behavior test
- another technically appropriate validation method

Some technologies may make tests difficult or impossible for certain implementation areas. In that case, the reason should be documented.

Tests should include documentation explaining:
- what behavior is being tested
- why the behavior matters
- which Task or Item the test belongs to
- which expected behavior future developers should preserve

The test does not always need to pass at this stage if the implementation does not yet exist.

The important point is that the intended behavior is documented and testable where possible.

---

## 18.5 First Pull Request: Structure, Documentation, And Tests

After the structure, Origin Developer documentation, and possible tests exist, the developer opens a Pull Request.

At this stage, the Pull Request is not primarily about finished implementation.

It is about confirming that:
- the structure is understandable
- the code documentation exists
- the Parent Item and Task references are present
- tests exist if technically possible
- test documentation exists where relevant
- the intended implementation direction is understandable

The Workflow Reviewer checks especially whether documentation and tests are present and understandable.

Implementation work should not continue until this review is accepted.

This rule exists to make documentation and tests easier to write before implementation complexity grows.

ODTS intentionally uses this workflow to help Origin Developers avoid neglecting documentation and tests during active implementation.

Many software projects slowly lose documentation quality because documentation is added too late or only after implementation is already complex.

By creating:
- implementation structure
- documentation
- and tests

before the main implementation phase, ODTS reduces the psychological and organizational barrier for maintaining documentation quality.

The pre-created structure makes it easier to continuously keep:
- documentation
- tests
- workflow traceability
- and implementation context

up to date while implementation evolves.

The workflow intentionally treats documentation and traceability as active implementation components instead of optional post-processing work.

---

## 18.6 Implementation Phase

After the Workflow Reviewer approves the initial structure, documentation, and tests, the developer begins implementation.

During implementation, the developer should continue to update documentation whenever:
- the implementation direction changes
- assumptions change
- additional code areas become involved
- Related Items or Related Tasks become relevant
- temporary solutions are introduced
- ToDos are created

If a new code area becomes part of the implementation, it should receive the same kind of traceability documentation.

The developer should not wait until the end to document what happened.

ODTS expects documentation to evolve with the code.

---

## 18.7 Mapping Code To Items And Tasks

During implementation, every meaningful code area should remain connected to its ODTS context.

This usually means documenting:
- the Parent Item
- the active Task
- Related Items if relevant
- Related Tasks if relevant
- ToDos if deferred work is introduced

This allows future developers to understand which part of the workflow introduced or changed a code section.

The goal is not to overload every line of code with metadata.

The goal is to make meaningful implementation blocks reconstructable.

---

## 18.8 Handling ToDos

If the developer discovers work that should not be completed immediately, a ToDo Task should be created.

A ToDo may describe:
- deferred cleanup
- postponed refactoring
- missing replacement work
- temporary workaround removal
- later test improvements
- future architecture cleanup

The code should reference the ToDo where appropriate.

Example:

```text
TODO: Replace this temporary adapter.
Related ToDo: #...
```

ToDos should not silently remain only in code comments if they represent meaningful future work.

They should become ODTS Tasks so that they remain visible in the workflow system.

---

## 18.9 Final Implementation Commit

When the Task implementation is complete, the developer creates a final implementation commit.

The commit should identify:
- exactly one Parent Item
- the completed Task
- Related Items or Related Tasks if relevant

Example:

```text
Item #...
Task #...

Implement initial ...
```

A commit must not mix work from multiple Parent Items.

If multiple Parent Items are affected, the work should be split into separate commits or separate Tasks.

---

## 18.10 Final Pull Request Review

After implementation is complete, the Pull Request receives a final review.

The Workflow Reviewer checks:
- whether the implementation matches the Task
- whether the code documentation still exists
- whether the documentation is still accurate
- whether tests exist if technically possible
- whether tests still describe the intended behavior
- whether Parent Item and Task references are present where needed
- whether ToDos were properly captured as ODTS Tasks
- whether no undocumented architectural decisions were introduced

The review explicitly includes documentation presence and documentation quality.

The review should additionally examine implementation quality itself.

This may include:
- security considerations
- potential security vulnerabilities
- unsafe implementation patterns
- maintainability
- architectural consistency
- readability
- traceability quality
- API stability
- dependency risks
- error handling
- resource management
- memory safety where relevant
- concurrency correctness where relevant
- test quality
- long-term maintainability

ODTS intentionally treats implementation quality as part of workflow quality.

A Task should not be considered complete only because code works.

A working implementation may still:
- introduce security risks
- reduce maintainability
- weaken traceability
- violate architectural goals
- create undocumented behavior
- introduce unstable interfaces

The Workflow Reviewer is therefore responsible not only for checking functionality, but also for evaluating whether the implementation quality is acceptable for long-term system evolution.

A Task is complete when:
- the implementation is complete
- the documentation is present
- the tests exist where possible
- the traceability is understandable
- the implementation quality is acceptable
- the Workflow Reviewer accepts the result


A Task should not be considered complete only because code works.

A Task is complete when:
- the implementation is complete
- the documentation is present
- the tests exist where possible
- the traceability is understandable
- the Workflow Reviewer accepts the result

---

## 18.11 Completion

After the final review is accepted, the Task may be moved to Done.

Done means that workflow work for this Task has ended.

If the Task was completed for an unusual reason, the reason should be documented in comments or notes.

The Parent Item may remain open if additional Tasks are still required.

The Parent Item may be moved to Done only after all required Tasks for that Item are complete or intentionally closed.

---

## 18.12 Summary Of The Workflow

The recommended ODTS implementation workflow is:

1. Select or receive an assigned Task.
2. Understand the Parent Item and related context.
3. Create the code structure first.
4. Add Origin Developer documentation to the code.
5. Add tests if technically possible.
6. Open a Pull Request for structure, documentation, and tests.
7. Receive Workflow Reviewer approval.
8. Implement the actual code.
9. Keep documentation and traceability updated during implementation.
10. Create ToDo Tasks for meaningful deferred work.
11. Create the final implementation commit.
12. Request final Pull Request review.
13. Complete the Task after documentation, tests, implementation, and traceability are accepted.

---

# 19. Future Evolution

Future ODTS evolution may include:
- improved automation
- better hierarchy visualization
- improved review workflows
- additional metadata systems
- deployment workflow improvements
- GitHub integration improvements
- external tooling support
- API-based workflow extensions

ODTS intentionally remains evolutionary and self-hosting.

