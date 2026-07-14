# Installing ODTS on GitHub

This guide starts a project from the prepared ODTS reference implementation using:

- the `ODTS-Specification` repository template;
- the `ODTS-Specification` GitHub Project template;
- organization-wide GitHub issue types and issue fields;
- repository-specific labels.

## Prerequisites

You need a GitHub organization and sufficient permissions to manage its planning settings. Organization owners configure issue types and issue fields. Repository and Project administrators configure the respective templates.

## 1. Configure organization issue types

Open the organization and navigate to **Settings → Planning → Issue types**.

Create or adapt these issue types:

| Issue type | Purpose |
| --- | --- |
| `ODTS EPIC` | Strategic goal, workflow goal, architectural direction, or requirement |
| `ODTS ITEM` | Coherent implementation area below an ODTS EPIC |
| `ODTS TASK` | Actionable work below an ODTS ITEM |

Issue types are organization-wide. Do not recreate them as labels or Project custom fields.

## 2. Configure organization issue fields

Navigate to **Settings → Planning → Issue fields** and create these single-select fields:

| Issue field | Options | Pin to |
| --- | --- | --- |
| `ODTS Epic Subtype` | `UserStory`, `Requirement` | ODTS EPIC |
| `ODTS Item Subtype` | `Feature`, `FeatureRequest`, `Bug`, `Documentation`, `Test` | ODTS ITEM |
| `ODTS Task Subtype` | `Work`, `ToDo` | ODTS TASK |

Make each subtype field visible only on its corresponding issue type. The native GitHub issue creation interface will then display the correct subtype without duplicating it inside issue forms.

Choose the visibility of every subtype field separately:

- **Public** when the value should be visible publicly where GitHub permits it;
- **Organization only** when it should be limited to organization members and authorized repository collaborators.

ODTS does not prescribe one visibility setting.

## 2.1 Optional team planning fields

Priority, Effort, Start date, and Target date are general organization fields, not part of the ODTS core. A team decides whether to use them and defines how their values are interpreted.

For **Priority**, a team MAY use the [Eisenhower Matrix](https://www.eisenhower.me/eisenhower-matrix/), which distinguishes urgency from importance. One possible option set is:

- `A`: important and urgent;
- `B`: important, not urgent;
- `C`: urgent, less important;
- `P`: Papierkorb—neither important nor urgent.

The team may choose a different priority model. **Effort** may represent a team-specific estimate; **Start date** and **Target date** may represent planned dates. Document the team's working agreement for every enabled field.

Choose **Public** or **Organization only** visibility independently for Priority, Effort, Start date, and Target date. The choice depends on whether the team wants that planning information visible outside the organization.

## 3. Create the repository from the template

Before the first installation, an administrator of `Nijida-Studio/ODTS-Specification` must enable **Template repository** in the repository's general settings.

1. Open the `Nijida-Studio/ODTS-Specification` repository on GitHub.
2. Choose **Use this template** and create a new repository in the target organization.
3. Enable Issues in the new repository.
4. Verify that the Epic, Item, and Task issue forms automatically select ODTS EPIC, ODTS ITEM, and ODTS TASK respectively.

The repository template intentionally contains no ODTS project description or contribution documentation that must be removed after creation. Add the new project's own README and contribution documentation when needed. Organization issue types and fields remain shared organization settings.

## 4. Adapt labels in the new repository

Labels are configured per repository, not per Project. Keep only labels that provide useful, quickly visible supplementary context.

ODTS reference labels are:

- `help wanted`
- `question`
- `needs review`
- `bootstrap`
- `blocked`
- `migration`

Add, remove, rename, and recolor labels for the repository as necessary. Do not use labels to duplicate Epic, Item, Task, subtype, priority, or status.

## 5. Create the GitHub Project from the template

1. In the target organization, create a new Project.
2. Select the organization template named **ODTS-Specification**. If it is not offered, open the reference Project and choose **Make a copy**.
3. Give the Project a name appropriate for the product or repository.
4. Optionally link the Project from the repository's **Projects** tab so it is easy to find. Set the repository as the Project's default repository if issues created directly in the Project should be created there.
5. Optionally link responsible teams when the Project should be listed for those teams or the team needs Project access.
6. Add the organization issue fields to the relevant Project views.
7. Verify the views, filters, sorting, grouping, and workflows.

When GitHub copies a Project, it copies views, Project custom fields, configured workflows other than auto-add workflows, and optional draft issues. It does not copy the original items, collaborators, team links, repository links, or auto-add workflows. Reconfigure those items after every installation.

## 6. Configure Project intake and workflows

Configure an auto-add workflow for each repository that participates in the Project. For a repository whose Issues are managed entirely with ODTS, use the filter `is:issue is:open`.

Repository and team links do not add Issues to the Project. Auto-add is a separate workflow under **Project menu → Workflows → Auto-add to project**. GitHub's built-in auto-add filter currently supports issue/PR state, labels, reasons, and assignees, but not the organization issue type. If a repository also contains non-ODTS Issues, either add them manually or use a genuinely contextual intake label; do not recreate Epic, Item, or Task as labels.

Verify the Project status values:

- `New`
- `Stasis`
- `In Progress`
- `Done`

Recommended minimum views:

- **Backlog** — Epic and Item, excluding Task;
- **Work** — Item and Task, excluding Epic;
- **My View** — work assigned to the current user;
- **All** — all ODTS issues, including completed work.

Do not create Project-level fields that duplicate organization issue fields. Add the organization fields to the Project when the team uses them.

## 7. Validate the installation

Create one test issue of each type and confirm:

- ODTS EPIC shows `ODTS Epic Subtype`;
- ODTS ITEM shows `ODTS Item Subtype`;
- ODTS TASK shows `ODTS Task Subtype`;
- optional Priority, Effort, Start date, and Target date fields appear only when configured for the team;
- every test issue is added to the Project;
- parent/sub-issue relationships can represent Epic → Item → Task;
- repository labels remain optional supplementary information;
- Project views display and filter the organization issue fields correctly.

Delete or close the test issues after validation.

## 8. Begin working with ODTS

For implementation work:

1. write and structure the issues;
2. create the code skeleton;
3. add rudimentary code documentation;
4. add tests before implementation where possible;
5. review that foundation;
6. implement and keep documentation and tests current.

## GitHub documentation

- [Managing issue types in an organization](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-types-in-an-organization)
- [Managing issue fields in your organization](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-fields-in-your-organization)
- [Syntax for issue forms](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
- [Copying an existing Project](https://docs.github.com/en/issues/planning-and-tracking-with-projects/creating-projects/copying-an-existing-project)
