# Contributing to [Drash Land](https://github.com/drashland/)

Contributors are always welcomed!

___This document was last updated on October 24, 2021. Please review this document if you have not reviewed it on or after this date.___

## Table of Contents

* [Changelog](#changelog)
* [Preparing Commit Messages](#preparing-commit-messages)
* [Reporting Bugs](#reporting-bugs)
* [Requesting New Features](#requesting-new-features)
* [Creating A Pull Request](#creating-a-pull-request)
* [Code Style Guidelines](#code-style-guidelines)
* [License](#license)

## Changelog

You can view all changes to this document [here](https://github.com/drashland/.github/commits/master/CONTRIBUTING.md).

## Commit Messages

We follow [https://www.conventionalcommits.org/](https://www.conventionalcommits.org/).

## Reporting Bugs

A bug is a *demonstrable problem* that is caused by the code. Good bug reports are extremely helpful, so thank you!

## Requesting New Features

We welcome all feature requests, but please take a moment to determine whether or not your idea fits with the scope and aims of the project. It is up to *you* to convince the maintainers of the merits of your feature request. Please provide as much detail and context as possible. Also, provide a use case for the feature. Providing a use case is ___required___.

## Creating a Pull Request

Please **ask first** before embarking on any significant pull request (e.g., implementing features, refactoring code, etc.). Otherwise, you risk spending a lot of time working on something that the maintainers might not want to merge.

Please make sure your pull request addresses the issue at hand ___without extra code bloat___. Do not create a pull request with a complex solution to a simple problem.

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project you want to work on.
2. Clone your fork.
    ```bash
    git clone https://github.com/<your-username>/<repo-name>.git
    ```
3. Go into your newly cloned directory.
    ```bash
    cd repo-name
    ```
4. Configure your remotes.
    ```bash
    # Assign the original repo to a remote called "upstream"
    git remote add upstream https://github.com/drashland/<repo-name>.git
    ```
5. If you cloned a while ago, get the latest changes from upstream:
    ```bash
    git checkout master
    git pull upstream master
    ```
6. Create a new branch (off of the `master` branch) to contain your additions, modifications, and/or deletions:
    ```bash
    git checkout -b <<issue-number>-branch-name>
    ```
7. Push your branch up to your fork:
    ```bash
    git push origin <<issue-number>-branch-name>
    ```
8. [Open a Pull Request](https://help.github.com/articles/about-pull-requests/) with a clear title and description against the `master` branch and follow the instructions in the pull request template.

    As a rule of thumb, ___always___ format your code using `deno fmt` before opening your pull request. If you forget to format your code, just add a commit with the message *deno fmt* (e.g., `git commit -m "deno fmt"`). The CI will fail if `deno fmt` is not performed.

Note: It is recommended that you *"clean up"* your commits before opening a pull request. Maybe take a look at `git rebase --interactive` to do this.

## Code Style Guidelines

Code should follow [Deno Style Guide](https://deno.land/manual/contributing/style_guide) with a few exceptions:

* Copyright headers are not required.
* Do not use `Deno.test()` when testing. Use [Rhum](https://github.com/drashland/rhum). Rhum should already be in all Drash Land projects (with the exception of [dmm](https://github.com/drashland/dmm) -- dmm should not use Rhum).

## License

By submitting a your code to the Drash Land organization, you agree to allow the maintainers to license your work under the terms of the [MIT License](./LICENSE).
