# Contributing to Socialler

## Branch Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Production — always stable and deployable |
| `develop` | Integration branch — base for all features |
| `feature/*` | New features (`feature/user-profile`) |
| `fix/*` | Bug fixes (`fix/feed-scroll-crash`) |
| `chore/*` | Maintenance, dependencies, tooling |
| `release/*` | Release preparation (`release/v1.2.0`) |
| `hotfix/*` | Critical production fixes |

Branch off from `develop`. Never commit directly to `main`.

## Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/).

```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```

### Types

| Type | When to use |
|------|-------------|
| `feat` | A new feature |
| `fix` | A bug fix |
| `chore` | Maintenance with no functional change |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `style` | Formatting, whitespace — no logic change |
| `test` | Adding or correcting tests |
| `docs` | Documentation only |
| `ci` | CI/CD pipeline changes |
| `perf` | Performance improvements |
| `revert` | Reverting a previous commit |

### Rules

- Use the imperative mood: `add feature` not `added feature`
- Keep the subject line under 72 characters
- Do not end the subject line with a period
- Reference issues in the footer: `Closes #42`

### Examples

```
feat(auth): add biometric login support
fix(feed): resolve infinite scroll crash on iOS
chore(deps): upgrade flutter to 3.22
refactor(profile): extract avatar component into separate widget
ci: add android release build workflow
docs: update contributing guidelines
```

## Pull Requests

- All PRs must target `develop`, never `main` directly
- Fill out the PR template completely
- Minimum **1 approval** required before merging
- Use **squash merge** to keep a clean history
- The PR title must follow Conventional Commits format
- Link related issues using `Closes #XXX`

## Code Review

- Review within **24 hours** on business days
- Be specific and constructive in comments
- Prefix non-blocking comments with `nit:`
- Approve only when you are confident the code is correct and follows conventions

## Releases

- A `release/vX.X.X` branch is cut from `develop`
- After QA, it is merged into `main` and tagged
- We follow [Semantic Versioning](https://semver.org): `MAJOR.MINOR.PATCH`

| Increment | When |
|-----------|------|
| `MAJOR` | Breaking changes |
| `MINOR` | New backward-compatible features |
| `PATCH` | Backward-compatible bug fixes |
