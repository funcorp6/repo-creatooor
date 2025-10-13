# Repo Creatooor

The repository creator workflow allows users to create new repositories with all the Wonderland securities configurations.

This guide is aimed at end users within your organization. If you're interested in configuring this for your organization, see [SETUP.md](./docs/SETUP.md).

## How to use it?

1. Click on the **Actions** button and then click on the "Repo creation" action.
2. Click on **Run Workflow**.
3. Fill in the mandatory field **Repository name**.
4. If you are creating the repo from a template fill in the template field (eg. defi-wonderland/solidity-hardhat-boilerplate), if not leave it empty.
5. Click on **Run Workflow**.
6. After some seconds, you will find your new repository on the organization's home page.

## Keep in mind

- The user that ran the workflow will have admin access to the repository. When adding more roles, **always prioritize adding teams** instead of individual collaborators.

## Repository Settings

- [✓] Disable "Allow rebase merging"
- [✓] Enable "Automatically delete head branches"
- [✓] Enable "Always suggest updating pull request branches"
- [✓] Disable Issues
- [✓] Disable Projects
- [✓] Disable Downloads
- [✓] Disable Wiki
- [✓] MIT is the default license
- [✓] Main branch protection
  - [✓] Enable "Require a pull request before merging"
  - [✓] Change "Require approvals" to 2
  - [✓] Enable "Dismiss stale pull request approvals when new commits are pushed"
  - [✓] Disable "Require review from Code Owners"
  - [✓] Enable "Require status checks to pass before merging"
  - [✓] Enable "Require branches to be up to date before merging"
  - [✓] Enable "Require signed commits"
- [✓] Dev branch protection
  - [✓] Enable "Require a pull request before merging"
  - [✓] Change "Require approvals" to 1
  - [✓] Enable "Dismiss stale pull request approvals when new commits are pushed"
  - [✓] Enable "Require status checks to pass before merging"
  - [✓] Enable "Require branches to be up to date before merging"
  - [✓] Enable "Require signed commits"

## Repo Doctor

In order to update an existing repository with the aforementioned settings, run the [Repo Doctor](https://github.com/defi-wonderland/repo-creatooor/actions/workflows/repo-doctor.yml). You only need to specify the repository name (e.g. solidity-hardhat-boilerplate) and the doctor will detect any deviations from the default config and try to fix them.
