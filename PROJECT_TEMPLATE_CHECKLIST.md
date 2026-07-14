# ODTS-Specification GitHub Project checklist

This checklist covers the work that must be completed in the GitHub UI for the **ODTS-Specification** Project template.

## Organization prerequisites

- [ ] Create or verify the organization issue types `ODTS EPIC`, `ODTS ITEM`, and `ODTS TASK`.
- [ ] Create `ODTS Epic Subtype` with `UserStory` and `Requirement`; pin it only to ODTS EPIC.
- [ ] Create `ODTS Item Subtype` with `Feature`, `FeatureRequest`, `Bug`, `Documentation`, and `Test`; pin it only to ODTS ITEM.
- [ ] Create `ODTS Task Subtype` with `Work` and `ToDo`; pin it only to ODTS TASK.
- [ ] Choose `Public` or `Organization only` visibility separately for every subtype field.

## Optional team extensions

- [ ] Decide whether the team uses the general organization fields Priority, Effort, Start date, and Target date. These are not ODTS core fields.
- [ ] If Priority follows the [Eisenhower Matrix](https://www.eisenhower.me/eisenhower-matrix/), document the chosen options, for example `A`, `B`, `C`, and `P`.
- [ ] Document the team's meaning and usage rules for every enabled optional field.
- [ ] Choose `Public` or `Organization only` visibility separately for every optional field.

## Project fields and status

- [ ] Add the organization issue fields to the Project.
- [ ] Keep GitHub's native `Type`, `Parent issue`, `Assignees`, and repository fields available where useful.
- [ ] Configure status values `New`, `Stasis`, `In Progress`, and `Done`.
- [ ] Remove Project custom fields that duplicate an organization issue field.

## Views

- [ ] Create **Backlog** for Epic and Item; exclude Task.
- [ ] Create **Work** for Item and Task; exclude Epic.
- [ ] Create **My View** filtered to the current user's assignments.
- [ ] Create **All** without excluding completed issues.
- [ ] Show `Type`, the relevant subtype fields, `Status`, `Assignees`, and `Parent issue` where useful; add optional team planning fields only when the team uses them.
- [ ] Verify that filters use native issue types and organization issue fields.

## Workflows

- [ ] Configure item-added behavior so new items start at `New` where appropriate.
- [ ] Configure closed issues to move to `Done` where appropriate.
- [ ] Decide and document how reopened issues leave `Done`.
- [ ] Configure a separate auto-add workflow for each repository participating in the Project; use `is:issue is:open` when all repository Issues follow ODTS.
- [ ] Confirm that Epic, Item, and Task issues are admitted. Do not assume that GitHub's auto-add filter can filter by organization issue type.
- [ ] Document that auto-add workflows must be recreated after copying the template.

## Template publication

- [ ] Link the Project from the reference repositories when it should appear in their **Projects** tab, and set a default repository if appropriate.
- [ ] Link responsible teams only when the Project should be discoverable by the team or the team requires Project access.
- [ ] Mark the Project as an organization template.
- [ ] Add it to the organization's recommended templates if desired.
- [ ] Test creating a new Project from the template.
- [ ] Confirm which settings do not copy: items, collaborators, team links, repository links, and auto-add workflows.

## Acceptance test

- [ ] Create one Epic, Item, and Task in a test repository.
- [ ] Set their subtype during creation using native GitHub fields; set optional team planning fields only when configured.
- [ ] Link them as Epic → Item → Task using parent/sub-issue relationships.
- [ ] Verify automatic Project intake.
- [ ] Verify all four views and their filters.
- [ ] Verify status automation for closing and reopening.
- [ ] Remove the test data before publishing the template.
