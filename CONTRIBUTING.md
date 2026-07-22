# Contributing

Thanks for your interest in contributing to Knot Forget.

## Getting Started

<!-- TODO: fill in build/test instructions once the Cargo project is initialized. -->

## Workflow

This project follows [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow):

1. `main` is always deployable and protected — no direct pushes.
2. Create a branch off `main` for each issue (see [Branch Naming](#branch-naming)).
3. Open a pull request early, even in draft, to track progress and link the related issue.
4. Merge via **squash merge** once required checks pass and the PR is reviewed.
5. The remote branch is deleted automatically on merge. Clean up your local copy too:
   ```
   git switch main
   git pull
   git branch -d <branch-name>
   ```

## Reporting Issues

- Search existing issues before opening a new one.
- Use the [issue template](.github/ISSUE_TEMPLATE/general.md) — include a clear summary and acceptance criteria.
- Label the issue with one of: `feat`, `fix`, `chore`, `refactor`, `test`, `docs`.

## Branch Naming

Use `<type>/<issue-number>-<short-description>`, where `<type>` matches one of the issue labels (`feat`, `fix`, `chore`, `refactor`, `test`, `docs`).

Example: `chore/0-project-repo-scaffold`

## Submitting Changes

1. Fork the repo and create a branch off `main`, following the naming convention above.
2. Make your changes with clear, atomic commits.
3. Open a pull request using the [PR template](.github/PULL_REQUEST_TEMPLATE.md), linking any related issue with `Closes #<issue>`.
4. Ensure required checks pass before requesting review.

`main` is protected: pull requests are merged via **squash merge** only, so keep your PR description accurate — it becomes the final commit message.

## Commit Style

Prefer [Conventional Commits](https://www.conventionalcommits.org/) (e.g. `fix: handle empty schedule`, `feat: add recurrence rule parser`) to keep history readable and align with the issue labels above.

## Code of Conduct

Be respectful and constructive. Report unacceptable behavior to the maintainer.
