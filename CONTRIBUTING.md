# Contributing at Vyntiq

These defaults apply to every Vyntiq repository that does not have its own `CONTRIBUTING.md`.

## Branches

- `main` is always releasable. It cannot be force-pushed or deleted.
- Work on a short-lived branch named `<type>/<short-description>`, for example `feat/sso-login` or
  `fix/report-timezone`. Keep it to days, not weeks.
- Rebase or update from `main` before asking for review.

## Commits

Use [Conventional Commits](https://www.conventionalcommits.org/):
`feat: …`, `fix: …`, `docs: …`, `test: …`, `refactor: …`, `perf: …`, `build: …`, `ci: …`, `chore: …`.
Explain **why** in the body, not only what; the diff already shows what.

## Pull requests

1. Open a pull request into `main`; use the template.
2. Keep it small enough to review in under 30 minutes. Split larger work.
3. All checks must be green: tests (`vyntiq-cd/test`), deployment (`vyntiq-cd/deploy`), secrets
   (`vyntiq-cd/secrets`) and the repository's own CI.
4. At least one other engineer reviews it. Code owners review changes to the code they own.
5. Squash-merge. The branch is deleted automatically.

## Continuous integration and deployment

Every repository is mirrored, tested and, if it is an application, deployed to an internal preview by
**Vyntiq CD**. Ask an organisation owner for the preview address and login. A `.vyntiq/cd.yml` file in the repository
controls tests, ports, health checks and extra domains (see the `vyntiq-cd` repository).

## Releases

Tag releases `vMAJOR.MINOR.PATCH` (Semantic Versioning), with release notes that say what changed and why.
