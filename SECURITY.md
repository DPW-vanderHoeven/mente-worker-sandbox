# Security Policy

## Supported Versions

This is a throwaway sandbox repository used for end-to-end testing of the
Mente worker. Only the `main` branch is supported; there are no tagged
releases and no backported security fixes.

## Reporting a Vulnerability

If you believe you have found a security vulnerability in this repository or
in the workflows it exercises, please report it privately. **Do not open a
public GitHub issue, discussion, or pull request that describes the
vulnerability.**

Preferred reporting channels, in order:

1. **GitHub private vulnerability reporting** — open a report from the
   repository's **Security** tab (`Security → Report a vulnerability`). This
   is the fastest way to reach the maintainers with an encrypted, tracked
   thread.
2. **Email** — send details to `security@mente.dev`. Please use the subject
   line `[SECURITY] mente-worker-sandbox` so the report is routed correctly.

Whichever channel you use, please include:

- A description of the issue and its potential impact.
- Steps to reproduce, a proof-of-concept, or a minimal test case.
- The commit SHA or branch where you observed the issue.
- Any suggested remediation, if you have one.
- How you would like to be credited (or a request to remain anonymous).

## Disclosure Process

Once a report is received, the maintainers will follow this process:

1. **Acknowledgement** — we aim to acknowledge new reports within **2
   business days**.
2. **Triage** — within **7 business days** we will confirm whether the
   report is a valid vulnerability, request any additional information we
   need, and assign a severity.
3. **Remediation** — we will work on a fix and keep the reporter updated on
   progress. Target timelines by severity:
   - Critical: patch within 7 days.
   - High: patch within 30 days.
   - Medium / Low: patch within 90 days.
4. **Coordinated disclosure** — once a fix is available, we will agree on a
   public disclosure date with the reporter. By default we disclose no
   sooner than 7 days after a fix has been released, and no later than 90
   days after the initial report, whichever comes first.
5. **Credit** — reporters who wish to be credited will be named in the
   release notes and, where applicable, in a published advisory.

## Safe Harbor

We consider security research and vulnerability disclosure activities
conducted in accordance with this policy to be authorized. We will not
pursue or support legal action against researchers who:

- Make a good-faith effort to avoid privacy violations, data destruction,
  and service disruption.
- Only interact with accounts they own or have explicit permission to
  access.
- Give us a reasonable amount of time to remediate before any public
  disclosure.
- Do not exploit the vulnerability beyond what is necessary to demonstrate
  the issue.

## Scope

In scope: source code and configuration in this repository.

Out of scope:

- Vulnerabilities in third-party dependencies that have not been modified
  here (please report those upstream).
- Denial-of-service issues that require excessive traffic.
- Social engineering of maintainers or contributors.

Thank you for helping keep this project and its users safe.
