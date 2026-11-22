# Contributing to Ndigo

Thanks for your interest in contributing. This is the organization-wide
baseline; individual repositories may extend it with their own
`CONTRIBUTING.md`, `AGENTS.md`, or `STYLE_GUIDE.md`, which take precedence.

## Before you start

- Read the target repository's own guidance first (`README.md`,
  `CONTRIBUTING.md`, `AGENTS.md`).
- For framework work, read
  [`ndigo/CONTRIBUTING.md`](https://github.com/ndigo/ndigo/blob/main/CONTRIBUTING.md)
  and [`ndigo/STYLE_GUIDE.md`](https://github.com/ndigo/ndigo/blob/main/STYLE_GUIDE.md).

## Baseline expectations

- **ESM only.** No CommonJS.
- **TypeScript** (where applicable): target `ES2022`, module resolution
  `Bundler`, Node.js ≥ 24, pnpm ≥ 12.
- **Formatting:** 4 spaces (TS/JS), single quotes, semicolons always,
  120-char width, ES5 trailing commas.
- **Naming:** `PascalCase` types, `camelCase` functions/variables,
  `UPPER_SNAKE_CASE` constants.
- **Tests:** add or update tests for behavior changes.
- **Commits:** use [Conventional Commits](https://www.conventionalcommits.org/)
  (`feat:`, `fix:`, `docs:`, `refactor:`, `chore:`, …).

## Pull requests

- Keep changes focused and small. One concern per PR.
- Run the repository's lint, type-check, and test commands before pushing.
- Reference the issue number in the PR title/body (`Closes #N`).

## Reporting bugs

Open a GitHub issue in the relevant repository with a minimal reproduction.

## Security

Do not open public issues for vulnerabilities — see
[`SECURITY.md`](./SECURITY.md).

## Code of conduct

This organization follows the
[Contributor Covenant](./CODE_OF_CONDUCT.md).
