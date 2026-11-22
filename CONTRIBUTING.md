# How we work

## Branches
- `main`: live version. Protected. Only receives PRs from `dev`.
- `dev`: integration and testing. Protected. Default branch.
- Task branches: created from `dev`, one task each, deleted after merge.
  - `feature/...` new feature
  - `fix/...` bug fix
  - `docs/...` documentation
  - `chore/...` setup or config
  - `ci/...` pipeline work
  - `infra/...` Docker, Terraform, Nginx

## Flow
task branch -> PR into `dev` -> tested together -> PR from `dev` into `main` -> deploy

## Pull requests
- Never push directly to `main` or `dev`.
- Every PR needs 1 approval from the other member.
- Keep PRs small: one task per PR.
- Every feature/fix branch must add or update tests. Broken tests are fixed before merging.

## Commit messages
- `feat: add join page`
- `fix: prevent duplicate tokens`
- `docs: update plan`
- `chore: add eslint`

## Secrets
- Never commit `.env`, passwords or API keys. Use `.env.example` for setting names only.
