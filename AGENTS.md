# AGENTS.md

## Project description

Knot Forget Core — lightweight event-scheduling core for Rust.

## Issue/PR labels

| Label | Meaning |
|---|---|
| `bug` | Something isn't working |
| `enhancement` | New feature or request |
| `chore` | Maintenance tasks |
| `refactor` | Code refactoring |
| `test` | Testing related |
| `docs` | Documentation |

## Issue template

New issues use the general template at [.github/ISSUE_TEMPLATE/general.md](.github/ISSUE_TEMPLATE/general.md), with sections: Summary, Acceptance Criteria, Additional Notes, References.

## PR template

New PRs use the template at [.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md), with sections: Summary, Changes, Related Issue/s, Testing, Breaking Changes, Checklist.

## Git workflow

This project follows [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow): `main` is always deployable, work happens on short-lived feature branches, and changes land via pull request.

1. Branch off `main` (e.g. `feature/x`, `fix/y`)
2. Commit and push changes
3. Open a PR against `main`
4. Merge (squash) once ready
5. Sync local `main` and delete the local branch (see below)

## Branch ruleset

The `main` branch is protected by a repository ruleset ([source](https://github.com/knot-forget/knot-core/rules/20570866)):

- Branch deletion blocked
- Non-fast-forward pushes (force pushes) blocked
- Changes must land via pull request
- Merges must use squash merge
- No required approving reviews (solo project)

Merged branches are auto-deleted on the remote. After a PR merges, sync locally:

```
git checkout main
git pull
git branch -d <branch-name>
```
