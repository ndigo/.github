# Security Policy

This is the default security policy for repositories in the **Ndigo**
organization. Repositories that ship their own `SECURITY.md` (such as the
[`ndigo`](https://github.com/ndigo/ndigo) framework) take precedence; their
policy supersedes this one.

## Reporting a vulnerability

**Do not open a public GitHub issue for a security vulnerability.**

- Preferred: open a private security advisory on GitHub (repository →
  Security → Advisories → "Report a vulnerability").
- Or email the maintainer: `jeff_rose@outlook.com`

Please include:

- the affected repository and version (or commit SHA)
- a minimal reproduction (code, request trace, or steps)
- an impact assessment (remote? auth bypass? data exposure? DoS?)

You will receive an acknowledgment within 72 hours and a fix timeline within
7 days. We ask that you coordinate disclosure until a patched version ships.

## Coordinated disclosure

We prefer Coordinated Disclosure: reporters receive advance notice of the fix,
and details are published a reasonable window after the patch ships. Credit is
given in the advisory unless anonymity is requested.

## Scope

This policy covers the code in Ndigo organization repositories. It does not
cover third-party dependencies, which are governed by their own maintainers.
Dependency advisories and the framework's detailed security model live in the
[`ndigo`](https://github.com/ndigo/ndigo) repository's `SECURITY.md`.
