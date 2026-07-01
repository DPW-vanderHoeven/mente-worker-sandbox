# Security Policy

## Reporting a Vulnerability

If you believe you have found a security vulnerability in this repository,
please report it privately. Do **not** open a public GitHub issue, pull
request, or discussion — that can expose other users before a fix is
available.

### How to report

- **Preferred:** open a private report via GitHub's
  [Security Advisories](../../security/advisories/new) for this repository.
- **Email:** send details to `dpw.vanderhoeven@gmail.com` with the subject
  line `SECURITY: <short summary>`.

Please include as much of the following as you can:

- A description of the issue and the impact you believe it has.
- Steps to reproduce (proof-of-concept code, commands, or a minimal repo).
- The affected commit, branch, or release.
- Any suggested mitigation, if you have one.
- Whether you would like to be credited in the advisory, and under what name.

### What to expect

| Stage | Target |
| --- | --- |
| Acknowledgement of your report | within 3 business days |
| Initial assessment and severity triage | within 7 business days |
| Status update cadence while under investigation | at least every 14 days |
| Fix or mitigation for confirmed high-severity issues | within 90 days of the report |

We will keep you informed as the investigation progresses, and coordinate a
disclosure timeline with you before publishing an advisory or fix.

## Scope

This policy applies to code hosted in this repository. Because this
repository is a sandbox used for end-to-end testing, it is not intended to
run production workloads; even so, we appreciate reports about anything
that could harm downstream users, such as:

- Secrets or credentials committed to history.
- Malicious or compromised dependencies.
- Vulnerable configuration templates that could be copied into real
  projects.

Reports about issues in third-party services or dependencies should be
directed to the upstream project. If you are unsure where to report,
contact us at the email above and we will help route it.

## Safe harbor

We will not pursue or support legal action against researchers who:

- Make a good-faith effort to comply with this policy.
- Avoid privacy violations, destruction of data, and disruption of
  service during their research.
- Give us reasonable time to investigate and remediate before any public
  disclosure.

Thank you for helping keep this project and its users safe.
