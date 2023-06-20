# GitHub Repo Template

![License](https://img.shields.io/github/license/rmarting/gh-repo-template?style=plastic)
![Main Lang](https://img.shields.io/github/languages/top/rmarting/gh-repo-template)
![Languages](https://img.shields.io/github/languages/count/rmarting/gh-repo-template)
![Last Commit](https://img.shields.io/github/last-commit/rmarting/gh-repo-template)
![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/rmarting/gh-repo-template)
[![➰ Sync labels 🏷️](https://github.com/rmarting/gh-repo-template/actions/workflows/sync-labels.yml/badge.svg)](https://github.com/rmarting/gh-repo-template/actions/workflows/sync-labels.yml)
[![🔖 Release Drafter 🔖](https://github.com/rmarting/gh-repo-template/actions/workflows/release-drafter.yml/badge.svg)](https://github.com/rmarting/gh-repo-template/actions/workflows/release-drafter.yml)
[![⚙️ Mark stale issues and pull requests ⚙️](https://github.com/rmarting/gh-repo-template/actions/workflows/stale.yml/badge.svg)](https://github.com/rmarting/gh-repo-template/actions/workflows/stale.yml)

This is a template repository including a set of items to be used as for any GitHub repository,
getting the most powerful tools and benefits from the GitHub's services.

Some of the items registered here are:

* Badges
* GitHub Workflows
* GitHub Templates
* Open Source Templates

## How to use it

This repo is declared as a GitHub repository template, it means that you can create a new GitHub repository
from here and getting from the scratch all the content already created here. This is an incredible way to initialize
any GitHub repo and get, from the first commit, a lot of content and automation process. Once you have the new
repository created, then you can customize each content with your own requirements, and details. Hope you
can find this stuff a powerful tool in your daily basics. At least, for me this is the new way of working with
GitHub.

These references will give you more details about how to create a repository from a template:

* [Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)

## Badges

Samples including in this readme file:

```markdown
![License](https://img.shields.io/github/license/rmarting/gh-repo-template?style=plastic)
![Main Lang](https://img.shields.io/github/languages/top/rmarting/gh-repo-template)
![Languages](https://img.shields.io/github/languages/count/rmarting/gh-repo-template)
![Last Commit](https://img.shields.io/github/last-commit/rmarting/gh-repo-template)
![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/rmarting/gh-repo-template)
[![➰ Sync labels 🏷️](https://github.com/rmarting/gh-repo-template/actions/workflows/sync-labels.yml/badge.svg)](https://github.com/rmarting/gh-repo-template/actions/workflows/sync-labels.yml)
[![🔖 Release Drafter 🔖](https://github.com/rmarting/gh-repo-template/actions/workflows/release-drafter.yml/badge.svg)](https://github.com/rmarting/gh-repo-template/actions/workflows/release-drafter.yml)
```

More details [here](https://blog.jromanmartin.io/2023/06/12/Improving-a-gh-repository.html) and in
the services provided by [Shields](https://shields.io/).

## GitHub Workflows

### Release Drafter

Workflows for automatic publishing releases and update changelogs. This workflow is implemented with the following files:

* [release-drafter.yml](.github/workflows/release-drafter.yml)
* [update-changelog.yml](.github/workflows/update-changelog.yml)

**NOTE**: There is an issue reported here about how to automatically trigger the update changelog workflow from the release workflow. The workaround to
fix it requires adding a new secret (`PERSONAL_ACCESS_TOKEN`) into your repo.

More details [here](https://blog.jromanmartin.io/2023/06/12/Improving-a-gh-repository.html).

### Close stale issues and PRs

[stale workflow](./github/workflows/stale.yml) will warn and close issue and PRs that have had not activity for a
specific amount of time.

### Continuous Integration in Quarkus/Maven repositories

Continuous Integration is a common practice to accelerate the development life cycle allowing to automate
a set of building and testing stages as soon a new commit is pushed into the repository. This will provide a fast
feedback about how is evolving the code by the different team members.

This repo include two different Continuous Integration workflows (or pipelines as I prefer call them):

* [CI for Pull Request](.github/workflows/ci-pr.yml) will build and test the content of any pull request, so we can confirm
that the source code can be integrated into the main branch successfully.
* [Full CI](.github/workflows/ci-full.yml) will implement a completed continuous integration workflow (building, testing, and packaging)
the artifacts and the native image of the application. The native image will be pushed into the [Quay.io](https://quay.io/), as container image repository.
This workflow requires to have two secrets (`QUAY_REPO_USERNAME`, and `QUAY_REPO_TOKEN`) with the right credentials to push images
into the container registry.

## GitHub Templates

## Issues Templates

* [New Bug](./.github/ISSUE_TEMPLATE/bug_report.md)
* [New Documentation](./.github/ISSUE_TEMPLATE/documentation.md)
* [New Feature](./.github/ISSUE_TEMPLATE/feature_request.md)
* [Others](./.github/ISSUE_TEMPLATE/housekeeping.md)

## Pull Request Template

* [Pull Request](./.github/pull_request_template.md)

## Open Source Templates

### Changelog

* [Changelog](./CHANGELOG.md)

### Code of Conduct

* [Code of Conduct](./CODE_OF_CONDUCT.md)
* [Contact](./CONTACT.md)

### Contributing

* [Contributing](./CONTRIBUTING.md)
