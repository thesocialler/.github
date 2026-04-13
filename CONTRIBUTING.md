# Contributing

This repository holds **organization-wide** guidelines (contribute the same way in **API** and **mobile** repos unless a repo overrides something locally).

## Branches

- `main` — production
- `develop` — integration; **branch new work from here**
- `feature/*`, `fix/*`, `chore/*`, `release/*`, `hotfix/*` — short, descriptive names

Do not commit directly to `main`.

## Commits

We use [Conventional Commits](https://www.conventionalcommits.org/): `type(scope): summary` (imperative, ~72 chars, no trailing period).

Common types: `feat`, `fix`, `chore`, `refactor`, `style`, `test`, `docs`, `ci`, `perf`, `revert`.

Example: `fix(feed): stop crash when refreshing on iOS`

Link issues in the body when relevant: `Closes #42`.

## Pull requests

- Target **`develop`**, not `main`
- Use the PR template (short summary + how you tested)
- Prefer **squash merge**; PR title should match Conventional Commits
- Get at least **one approval** before merge

## Reviews

Aim to respond within a business day. Be specific; use `nit:` for optional nits. Approve when the change is correct and fits project conventions.

## Releases

Release branches follow `release/vX.Y.Z`. After QA, merge to `main` and tag. Versioning follows [SemVer](https://semver.org).
