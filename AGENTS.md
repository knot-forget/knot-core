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

## Branch ruleset

The `main` branch is protected by a repository ruleset ([source](https://github.com/knot-forget/knot-core/rules/20570866)):

- Branch deletion blocked
- Non-fast-forward pushes (force pushes) blocked
- Changes must land via pull request
- Merges must use squash merge
- No required approving reviews (solo project)
