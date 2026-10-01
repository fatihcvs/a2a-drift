# Security policy

## Scope and supported versions

This policy covers vulnerabilities in a2a-drift's Python package, command-line
interface, and repository-provided integrations. Report problems in an agent
being inspected to that agent's operator or maintainer instead.

Security fixes target the latest released version and the current `main`
branch. Older releases have no separate backport commitment; upgrade to the
latest release before checking whether a problem is still reproducible.
A clean drift report is not a security audit of the inspected agent.

## Report a vulnerability privately

Email **yunare@gmail.com**, the maintainer contact published in
[pyproject.toml](pyproject.toml), with a subject beginning `a2a-drift security`.
Do not put exploit details, credentials, or sensitive agent data in a public
issue, pull request, or discussion. GitHub private vulnerability reporting is
not currently enabled for this repository; use email rather than assuming a
private reporting form is available.

Include:

- The affected release or commit, Python version, and operating system.
- The affected component, expected behavior, and security impact.
- Minimal reproduction steps or a small, sanitized proof of concept.
- Relevant logs or agent-card examples with tokens, personal information,
  and private endpoints removed.
- Any suggested mitigation and your preferred contact and credit details.

Only test systems you own or are authorized to test. Never send private keys,
production credentials, or a full private dataset to demonstrate a problem.

## Response and coordinated disclosure

Maintainer availability determines response times; there is no guaranteed
response or fix SLA. If you have not received an acknowledgment after seven
days, follow up on the same email thread without publishing sensitive details.

Coordinate disclosure timing with the maintainer so a fix or mitigation can
be prepared and affected users can act. Agree on a publication date during
triage rather than assuming a fixed embargo or that an unanswered report has
been resolved. Discuss attribution before publication.

## Security fixes and releases

Accepted fixes follow the project's normal versioned release process. Consult
[releases](https://github.com/yunaremaia/a2a-drift/releases) and
[CHANGELOG.md](CHANGELOG.md) for published fixes and upgrade information.
Public release notes should identify affected and fixed versions and any
available mitigation once coordinated disclosure is ready; sensitive report
details stay private until then.
