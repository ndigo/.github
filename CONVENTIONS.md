# Ndigo Code Conventions (Baseline)

This document states the **organization-wide baseline** for code in Ndigo
repositories. It is intentionally short and generic. Framework repositories
(notably [`ndigo`](https://github.com/ndigo/ndigo)) extend it with a
detailed, framework-specific guide:

- Full guide: <https://ndigo.dev/concepts/style-guide/>
- Source: [`ndigo/STYLE_GUIDE.md`](https://github.com/ndigo/ndigo/blob/main/STYLE_GUIDE.md)

When a repository's own `STYLE_GUIDE.md` or `AGENTS.md` conflicts with this
baseline, the repository-specific document wins for that repository.

## Module system

- **ESM only.** No CommonJS (`require`). Every package declares
  `"type": "module"`.
- **TypeScript**, target `ES2022`, module resolution `Bundler`.
- **Node.js ≥ 24**, **pnpm ≥ 12**.

## Formatting

Enforced with `oxfmt` (or the equivalent in non-TypeScript repos):

- Indentation: 4 spaces for TS/JS, 2 spaces for JSON/YAML.
- Single quotes `'`.
- Semicolons always.
- Print width: 120 characters.
- Trailing commas: ES5 style.

## Naming

- **Classes / interfaces / types:** `PascalCase`.
- **Methods / variables / functions:** `camelCase`.
- **Constants:** `UPPER_SNAKE_CASE`.
- **Private fields:** `#` syntax.
- **Files:** `kebab-case.ts` for source, `kebab-case.spec.ts` for tests.
- **Acronyms:** all-uppercase in types (`HTTPTransformer`), all-lowercase or
  all-uppercase in identifiers (`httpTransformer`, `myHTTPData`).

## Predicates and duck-typing

- `is*` — type/identity checks using `typeof` or `instanceof`. Asks
  "is this an instance of X?"
- `like*` — structural/shape checks using property presence. Asks "does
  this behave like X?" Never use `instanceof` as the primary check in a
  `like*` function.

## Documentation

- **TSDoc** (`/** ... */`) on every public export.
- One public type per file where practical.
- Files should stay under ~300 lines; refactor above that.
- Comments carry **rationale**, not restatement: document _why_, not _what_.

## Self-documenting code

- Names carry meaning. Bare `as any`, `as unknown as T`, and
  `// @ts-ignore` require a one-line reason.
- `// NOTE:` marks technical debt.
- Assertions should state their rationale where it is not obvious.

## Error handling

- Prefer specific error classes over generic `Error` where the language or
  framework provides them.

## When in doubt

For framework-specific rules (decorators, role-based suffixes, utility
organization, library integration layers, oxlint enforcement), consult the
repository's own `STYLE_GUIDE.md` and `AGENTS.md`, or the published guide at
<https://ndigo.dev/concepts/style-guide/>.
