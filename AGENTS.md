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

1. Branch off `main` (see naming convention below)
2. Commit and push changes
3. Open a PR against `main`
4. Merge (squash) once ready
5. Sync local `main` and delete the local branch (see below)

### Branch naming

Branches are named `<type>/<issue-number>-<short-description>`, where `<type>` matches the issue/PR labels, with `enhancement` and `bug` shortened to `feat` and `fix`. The issue number may be omitted for small changes that don't have an associated issue:

| Type | Label equivalent |
|---|---|
| `feat` | `enhancement` |
| `fix` | `bug` |
| `chore` | `chore` |
| `refactor` | `refactor` |
| `test` | `test` |
| `docs` | `docs` |

e.g. `feat/42-recurring-events`, `fix/57-timezone-offset`, `docs/readme-typo`

### Commit conventions

Commits follow [Conventional Commits](https://www.conventionalcommits.org/): `<type>[optional scope]: <description>`, using the same `<type>` values as branch naming.

- `feat:` a new feature
- `fix:` a bug fix
- `chore:` maintenance tasks
- `refactor:` code change that neither fixes a bug nor adds a feature
- `test:` adding or correcting tests
- `docs:` documentation only changes
- Append `!` after the type/scope (e.g. `feat!:`) or add a `BREAKING CHANGE:` footer for breaking changes

e.g. `feat(scheduler): support recurring events`, `fix: correct timezone offset calculation`

### Commit granularity

Commit by concern, not by file: each commit should represent one logical change and include every file it touches, even across directories. Avoid splitting a single concern into multiple commits, and avoid bundling unrelated concerns into one.

Do not split implementation, tests, and documentation for the same concern into separate commits — each commit should stay buildable and revertable on its own. Only give docs or tests their own commit when they address a genuinely unrelated concern.

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
