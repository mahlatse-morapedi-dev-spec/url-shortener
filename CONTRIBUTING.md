# Contributing to LinkLite

## Development Workflow

All development changes should be tracked using Git.

## Branch Naming

Use descriptive branch names.

Examples:

- `feature/url-shortening`
- `feature/url-redirection`
- `fix/duplicate-url-handling`
- `docs/system-design`

## Commit Convention

LinkLite follows Conventional Commits.

Format:

`<type>: <description>`

Common types:

| Type | Purpose |
|---|---|
| feat | New functionality |
| fix | Bug fixes |
| docs | Documentation changes |
| test | Testing changes |
| refactor | Code restructuring |
| chore | Maintenance tasks |
| perf | Performance improvements |

Examples:

- `feat: implement URL shortening endpoint`
- `fix: handle duplicate URL submissions`
- `docs: update database design`

## Testing Requirements

New functionality should include appropriate automated tests.

All relevant tests must pass before merging changes.

## Documentation Requirements

Changes affecting system architecture, API behaviour, database structure or configuration must be reflected in the relevant documentation.

## Release Requirements

Releases must:
- Have a corresponding Git tag.
- Follow Semantic Versioning.
- Include updated release notes.
- Have an updated VERSION file.
- Pass relevant automated tests.
