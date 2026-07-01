# Security Policy

We take security seriously and appreciate reports from the community that help
keep this project and its users safe. This document describes how to report a
vulnerability and what to expect during the coordinated disclosure process.

## Supported Versions

Only the latest commit on the `main` branch receives security fixes. Older
branches, tags, and forks are not maintained.

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security problems.** Public
issues can expose users before a fix is available.

Report vulnerabilities through one of the following private channels, in order
of preference:

1. **GitHub Private Vulnerability Reporting** — open a private advisory via the
   repository's **Security → Advisories → Report a vulnerability** page. This
   is the preferred channel because it keeps the report, discussion, and fix
   tracked together.
2. **Email** — if GitHub reporting is unavailable, contact the maintainer at
   `dpw.vanderhoeven@gmail.com` with the subject line
   `SECURITY: <short summary>`. PGP-encrypted mail is welcome; request the
   maintainer's key in an initial unencrypted message if needed.

### What to include

To help us triage quickly, please include as much of the following as you can:

- A clear description of the issue and its potential impact.
- The affected component, file paths, commit hash, or version.
- Step-by-step reproduction instructions, ideally with a minimal proof of
  concept.
- Any known mitigations or workarounds.
- Whether the issue is already public or has a CVE assigned.

## Disclosure Process

We follow a coordinated disclosure model:

1. **Acknowledgement** — we aim to acknowledge receipt of your report within
   **3 business days**.
2. **Triage** — within **10 business days** we will confirm whether the report
   is a valid vulnerability, request more information, or explain why we do
   not consider it in scope.
3. **Fix development** — for accepted reports we work on a fix privately.
   Target timelines depend on severity:
   - **Critical / High:** patch targeted within 30 days of triage.
   - **Medium:** patch targeted within 60 days of triage.
   - **Low:** patch targeted within 90 days of triage, or bundled with the next
     regular release.
4. **Coordinated release** — once a fix is ready we agree on a disclosure date
   with the reporter. We aim to publish a GitHub Security Advisory, request a
   CVE where appropriate, and credit the reporter (unless anonymity is
   preferred).
5. **Public disclosure** — we default to a **90-day** maximum embargo from
   initial acknowledgement. If a fix is not ready by then we will contact the
   reporter to agree on an extension or coordinated early disclosure.

## Safe Harbor

We will not pursue legal action against researchers who:

- Make a good-faith effort to comply with this policy.
- Avoid privacy violations, degradation of user experience, and disruption to
  production systems.
- Do not exfiltrate data beyond what is necessary to demonstrate the issue.
- Give us a reasonable window to remediate before public disclosure.

## Out of Scope

The following are generally **not** treated as security vulnerabilities:

- Reports generated purely by automated scanners without demonstrated impact.
- Missing security headers or best-practice hardening on non-production
  endpoints without a concrete exploitation path.
- Social engineering, physical attacks, or attacks requiring privileged local
  access.
- Denial of service caused by excessive traffic volume.

## Thank You

We are grateful to the researchers and users who take the time to report
security issues responsibly. Your work helps protect everyone who depends on
this project.
