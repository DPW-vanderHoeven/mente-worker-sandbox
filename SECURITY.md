# Security Policy

## Reporting a Vulnerability

If you believe you have discovered a security vulnerability in this repository,
please report it privately so we can investigate and address it before it is
publicly disclosed.

**Please do not open a public GitHub issue for security vulnerabilities.**

To report a vulnerability, email **dpw.vanderhoeven@gmail.com** with the
following information:

- A description of the vulnerability and its potential impact.
- Steps to reproduce the issue (proof-of-concept code, sample requests, or a
  minimal test case if applicable).
- The affected version, branch, or commit.
- Any suggested remediation, if known.
- Your name and contact details, and whether you would like to be credited in
  the eventual advisory.

You should expect an initial acknowledgement within **3 business days** of your
report. We will follow up with a triage assessment (severity, scope, and next
steps) within **10 business days**.

## Coordinated Disclosure

We follow a coordinated (responsible) disclosure process:

1. **Report received.** We acknowledge the report and begin investigation.
2. **Triage.** We confirm the issue, determine severity, and identify affected
   versions.
3. **Fix development.** We develop and test a fix in a private branch. We may
   contact you for clarification or to validate a candidate fix.
4. **Coordinated release.** We publish the fix and, where appropriate, a
   security advisory crediting the reporter (unless anonymity is requested).
5. **Public disclosure.** Details of the vulnerability are disclosed publicly
   after users have had a reasonable opportunity to update — typically **90
   days** from the initial report, or sooner if a fix is released earlier.

We ask that reporters:

- Give us reasonable time to investigate and remediate before any public
  disclosure or sharing of details with third parties.
- Avoid privacy violations, data destruction, service degradation, or any
  interruption to production systems during your research.
- Only interact with accounts or data you own or have explicit permission to
  access.

## Scope

This policy applies to the code contained in this repository. Vulnerabilities
in third-party dependencies should generally be reported to their respective
maintainers; if you believe our use of a dependency introduces a specific
vulnerability here, please report it to us as well.

## Safe Harbor

We consider security research conducted in good faith and in accordance with
this policy to be authorized. We will not pursue or support legal action
against researchers who comply with the guidelines above. If in doubt about
whether a specific action is covered, contact us at the email above before
proceeding.
