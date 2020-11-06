# Contributing to [Drash Land](https://github.com/drashland/)

___This document was last updated on November 6, 2020. Please review this document if you have not reviewed it on or after this date.___ 

## Table of Contents

* [Branch Naming Conventions](#branch-naming-conventions)
* [Bug Reports](#bug-reports)
* [Feature Requests](#feature-requests)
* [Pull Requests](#pull-requests)
* [Code Style Guidelines](#code-style-guidelines)

## Branch Naming Conventions

The issue number should always be the first item in the branch name. For example, checking out a new branch for issue #123 looks like:

```shell
git checkout -b "123-my-branch"
```

The issue number should be followed by a description that matches the work needing to be done in the issue. For example, if issue #123 involves fixing a bug related to response.render(), then checking out a new branch would look like:

```shell
git checkout -b "123-fix-response-render-method"
```

## Bug Reports

A bug is a *demonstrable problem* that is caused by the code in the repository. Good bug reports are extremely helpful, so thanks!

## Feature Requests

We welcome all feature requests, but please take a moment to determine whether or not your idea fits with the scope and aims of the project. It is up to *you* to convince the maintainers of the merits of your feature(s). Please provide as much detail and context as possible.

## Pull Requests

Please **ask first** before embarking on any significant pull request (e.g. implementing features, refactoring code). Otherwise, you risk spending a lot of time working on something that the maintainers might not want to merge.

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
6. Create a new branch (off of the master branch) to contain your additions, modifications, and/or deletions:
    ```bash
    git checkout -b <<issue-number>-branch-name>
    ```
7. Push your branch up to your fork:
    ```bash
    git push origin <<issue-number>-branch-name>
    ```
8. [Open a Pull Request](https://help.github.com/articles/about-pull-requests/) with a clear title and description against the `master` branch and follow the instructions in the pull request template.

    As a rule of thumb, ___always___ format your code using `deno fmt` before opening your pull request. Run this as your last single commit. If you forgot to correctly format it, just add a commit with the message *deno fmt* (e.g., `git commit -m "deno fmt"`). The CI will fail if `deno fmt` is not performed.

***Note:*** It is recommended that you *"clean up"* your commits before opening a pull request. Maybe take a look at `git rebase --interactive` to do this.

## Code Style Guidelines

Code should follow [Deno Style Guide](https://deno.land/manual/contributing/style_guide) with a few exceptions:

* Copyright headers are not required.
* Do not use `Deno.test()` when testing. Use [Rhum](https://github.com/drashland/rhum). Rhum should already be in all Drash Land projects (with the exception of [dmm](https://github.com/drashland/dmm) -- dmm should not use Rhum).

## License

By submitting a your code to the Drash Land organization, you agree to allow the maintainers to license your work under the terms of the [MIT License](./LICENSE).
