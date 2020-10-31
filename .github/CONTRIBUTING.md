# Contributing to [Drash Land](https://github.com/drashland/)

## Bug Reports

A bug is a *demonstrable problem* that is caused by the code. Good bug reports are extremely helpful, so thanks!

If you want to report a bug, click [here](./issues).

## Feature Requests

We welcome all feature requests, but please take a moment to determine whether or not your idea fits with the scope and aims of the project. It is up to *you* to convince the maintainers of the merits of your feature(s). Please provide as much detail and context as possible. If you want to request a feature, click [here](./issues).

## Pull Requests

Please **ask first** before embarking on any significant pull request (e.g. implementing features, refactoring code). Otherwise, you risk spending a lot of time working on something that the maintainers might not want to merge.

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project, clone your fork, and configure the remotes:
    ```bash
    # Clone your fork of the repo into the current directory
    git clone https://github.com/<your-username>/<repo-name>.git
    # Navigate to the newly cloned directory
    cd repo-name
    # Assign the original repo to a remote called "upstream"
    git remote add upstream https://github.com/drashland/<repo-name>.git
    ```
2. If you cloned a while ago, get the latest changes from upstream:
    ```bash
    git checkout master
    git pull upstream master
    ```
3. Create a new branch (off of the master branch) to contain your additions, modifications, and/or deletions:
    ```bash
    git checkout -b <<issue-number>-branch-name>
    ```
4. Push your branch up to your fork:
    ```bash
    git push origin <<issue-number>-branch-name>
    ```
5. [Open a Pull Request](https://help.github.com/articles/about-pull-requests/) with a clear title and description against the `master` branch and follow the instructions in the pull request template.

***Note:*** It is recommended that you *"clean up"* your commits before opening a pull request. Maybe take a look at `git rebase --interactive` to do this.

## Code Guidelines

- Code should follow [Deno Style Guide](https://deno.land/manual/contributing/style_guide).

- As a rule of thumb, always format your code using `deno fmt` before opening your pull request. Run this as your last single commit. If you forgot to correctly format it, just add a commit with the message *deno fmt* (`git commit -m "deno fmt"`). The CI will fail if `deno fmt` is not performed.

## License

By submitting a patch, you agree to allow the maintainers to license your work under the terms of the [MIT License](../LICENSE).
