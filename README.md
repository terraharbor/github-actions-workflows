# github-actions-workflows

GitHub Actions workflows for the TerraHarbor repositories.

## Table of Contents

- [github-actions-workflows](#github-actions-workflows)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)

## Overview

The main purpose of this repository is to centralize workflows that commonly used throughout the remainder of repositories. This eases maintainability and ensures each repository uses workflows that are up-to-date.

> [!TIP]
> Any workflow with a `workflow_call` trigger, is callable by workflows on other repositories. Notice that some of the workflows have required inputs.

There is, however, a special workflow in this repository: the `renovate.yaml` workflow. It runs periodically and checks every other repository for outdated dependencies (either on code or workflows). **If an update is found, it creates a pull request to update the dependency, which the maintainer then needs to review and merge manually**.

> [!IMPORTANT]
> For a repository to be included in the automatic updates, it needs to contain a `.renovaterc.json` on its root, even it's an empty one with `{}` as content.
