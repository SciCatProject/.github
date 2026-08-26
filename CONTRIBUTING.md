# Contributing to SciCat Projects

## Abbreviations and Links

Core = [SciCat Core](../project-components/SCICAT-CORE.md)

## Description

Core repositories follow the procedure indicated below for contributions.

Other SciCat repositories (Supported Projects and Non-Code repositories) are highly encouraged to follow the same procedure. If they decide otherwise, they should clearly state the contribution procedure in the CONTRIBUTING.md files included in the root folder of the repository.
Each repository should also indicate who are the maintainers of the repository and list them, together with their responsibility, in the MAINTAINERS.md file.

## Merge Permissions

Each repository should have a merging group indicating who has merge permissions.
The SciCat project leaders and the project leaders are automatically part of the project merge group.
Other contributors can be part of the merge group. A contributor shall submit a dedicated request in order to be added to such group.
Membership to the merge group is managed by the project leaders.

The SciCat core repositories are managed as a single project. They have a single maintainers group and a single merge group.

## AI Contribution

In this paragraph we address the use of AI in developing code for the Project.
The following rules must be followed if AI is used in any PR contributed to the Project:

- We do not support automating raising of pull requests by Agentic AI.
  All PRs must be submitted by a human or a trusted tool bot e.g. dependabot.
- The human submitter must review all AI-generated code
- Compliance with licensing requirements must be ensured
- The PR can be accepted only if at least one human reviewer has reviewed it and signed it off
- Human submitter and reviewers will take full responsibility for the contribution
- PR can be merged only by a person belonging to the Merge group
- The PR should contain attribution on which AI service and agent has been used.
  The attribution should be in the following format:
  Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]


## SciCat Contributing Workflow

### 1. Main Branch Policy

* The latest stable version of the code **must reside in `master` or `main`**.
* The `master` / `main` branch **is protected** and **must not be modified directly**.

### 2. Development Workflow

* All work (new features, bug fixes, documentation, or other changes) **must be done in a dedicated branch or a repository fork** depending on the user access.
* Dedicated forks **must allow read and write access for maintainers**.
* No changes may be introduced in `main` / `master` without a **Pull Request (PR)**.

### 3. Pull Request Requirements

* Every change **must be submitted via a Pull Request** targeting `master` / `main`.
* The **author of a Pull Request must not merge their own PR**.
* The author of a Pull Request must indicate the impact of the changes
* Reviews should be requested from official project reviewers, and The wider community when appropriate.
* When possible, reviewers should have the required skills to provide an unbiased and expert feedback.

### 4. Impact Classification

- Each Pull Request **must be classified by its impact**: _large_ or _lower_.
- **Responsibility for impact classification lies with the author**
- Repository maintainers can review and change the Pull Request impact.
- The impact classification **may be updated after submission**, provided:
  - A valid justification is given, and
  - The change is publicly documented in the PR.

### 5. Review Rules

#### Large-Impact Pull Requests

- Must be reviewed by **at least two maintainers**.
- At least **one reviewer must be from a different institution or group**.
- At least one review should be a **technical review** giving detailed feedback about code changes. The second review may be a **conceptual review** which evaluates the appropriateness of the PR for inclusion in SciCat, but without evaluated the implementation details. Conceptual reviews should be clearly indicated in the review comments.
- Review period: **minimum 1 week, maximum 2 weeks**.

#### Lower-Impact Pull Requests

- Must be reviewed by **at least one maintainer**.
- Review period: **maximum 2 weeks**.

### 6. Approval, CI, and Merge

- A Pull Request **must be approved** and **pass all CI checks** before it can be merged.
- **Only maintainers with the “Pull Request Master” role** may merge approved Pull Requests.

### 7. Branch Cleanup

- The source branch **must be deleted** once the Pull Request is merged or closed.

![Contributing Worflow](./contributing.png)
