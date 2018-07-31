# Product Delivery Project Management Standards

## General

* **SHOULD**

  * be managed in Github under the [mozilla](https://github.com/mozilla) organization.

## Repositories

* **MUST**

  * Have a "product-delivery" [topic](https://help.github.com/articles/about-topics/)
  * Have a README document. It should follow our standard [readme template (tbd)]
  * Have a LICENSE text file

* **SHOULD**

  * Be licensed under the Mozilla Public License version 2.0
  * Use Markdown for README format
  * Use a GitHub Project to track statuses of issues
  * Use CircleCI for continuous integration
  * Follow [Dockerflow specification](https://github.com/mozilla-services/Dockerflow)
  * Use [bors](https://bors.tech) for merging.
  
* **MAY**

  * Have a contributors.txt describing contribution guidelines
    * Use "mentored" tags to [expose contributor friendly bugs to
      Bugsahoy](https://wiki.mozilla.org/BugsAhoy)
  * Use third party development tools for code coverage, documentation, etc.

## Projects

* **SHOULD**

  * Be used to track issue status with the columns:

    * Backlog, with [automation](https://help.github.com/articles/configuring-automation-for-project-boards/)
      set to the "To Do" preset
    * In Progress, with automation set to the "In Progress" preset
    * Blocked, with automation set to the "None" preset
    * Complete, with automation set to the "Done" preset

  * Have a description with details about the goals of the project

## Milestones

* **MAY**

  * Be used to group issues together

## Issues

* **MUST**

  * Have an assignee when labeled as P1

* **SHOULD**

  * Have a label identifying it, e.g: bug, proposal, fix, etc. (see triaging and labeling issues)

* **MAY**

  * Be assigned to a milestone
  * Use [tasks lists](https://help.github.com/articles/about-task-lists/) for
    large / complex issues with many small tasks

## Triaging and Labeling Issues

We have a core set of labels. These labels are not exhaustive but make up
a convention for available labels across all Product Delivery projects.

* Priority level: `P1`, `P2`, `P3`, `P5`

  * Follow the [Bug Masters guidance](https://wiki.mozilla.org/Bugmasters/Process/Triage)
    for triaging issue
  * `P1` - Fix in the current release or iteration
  * `P2` - Fix in the next release or iteration
  * `P3` - Backlog
  * `P5` - Will not fix, but will accept a patch
  * Color code: ![#ffa32c](https://placehold.it/15/ffa32c/000000?text=+) `#ffa32c`

* Problem Identifications: `bug`, `security`

  * Identifies the type of fix required.
  * Color code: ![#b60205](https://placehold.it/15/b60205/000000?text=+) `#b60205`

* Enhancement identifications: `improvement`, `documentation`, `fix`, `new-feature`

  * Identifies: pull requests, feature requests
  * Color code: ![#0e8a16](https://placehold.it/15/0e8a16/000000?text=+) `#0e8a16`

* Request for comments: `question`, `proposal`, `support-request`

  * Proposing new features/changes or requesting info / support
  * Used to capture conversations and decisions. Pull requests should have a “closes #<issue>” which would link the proposal.
  * Color code: ![#1d76db](https://placehold.it/15/1d76db/000000?text=+) `#1d76db`

* `<components/misc labels>`

  * Use for components, miscellaneous type labels as needed by the project
  * Color code: ![#5319e7](https://placehold.it/15/5319e7/000000?text=+) `#5319e7`

## Directly Responsible Individual ("DRI")

Read the [primer about Apple's DRI model](https://www.quora.com/Apple-company/How-well-does-Apples-Directly-Responsible-Individual-DRI-model-work-in-practice).

The Directly Responsible Individual model is a simple model to clarify
communications and accountability. We use GitHub's assignee as the
DRI for the issue.

### Expectations of a DRI for a project:

* Make pragmatic decisions (priorities, ship dates, etc)
* Ensure all issues are triaged
* Prioritized the issue appropriately (`P1`, `P2`, `P3`, `P5`), milestones,
  etc.
* Assign issues to DRI on Issues (delegate)
* Remove project level blockers (resourcing, miscommunication, etc)

### Expectations of an DRI for an issue:

* Drive the issue to a **closed** state. (fixed or wontfix).
* Unblocking the issue
* Work on or delegate tasks to complete the issue
* Keep the issue's status in a project current (backlog, in progress, blocked,
  etc)
