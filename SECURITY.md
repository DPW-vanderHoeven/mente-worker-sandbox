# Security Policy

## Reporting a Vulnerability

Please **do not** open a public GitHub issue for security vulnerabilities.

Report suspected vulnerabilities privately through GitHub's private
vulnerability reporting:

1. Go to the [Security tab](https://github.com/DPW-vanderHoeven/mente-worker-sandbox/security)
   of this repository.
2. Click **Report a vulnerability**.
3. Provide a description, reproduction steps, affected versions or commits,
   and any suggested mitigation.

If you cannot use GitHub's private reporting, email
**dpw.vanderhoeven@gmail.com** with the subject line `SECURITY:
mente-worker-sandbox` and the same details.

Please include:

- A clear description of the issue and its impact.
- Step-by-step reproduction (proof-of-concept preferred).
- The commit SHA or version where you observed the issue.
- Your contact information for follow-up.

## Disclosure Process

We follow a coordinated disclosure model:

| Stage | Target time from initial report |
| --- | --- |
| Acknowledge receipt | Within 3 business days |
| Initial triage and severity assessment | Within 7 business days |
| Status update cadence during investigation | At least every 14 days |
| Fix or mitigation available | Within 90 days for most issues |
| Public disclosure | After a fix ships, coordinated with the reporter |

If we cannot resolve an issue within 90 days, we will contact the reporter to
agree on an extended timeline. Critical issues under active exploitation will
be prioritized and may be disclosed sooner alongside emergency mitigations.

## Scope

In scope:

- Source code in this repository.
- Build and release artifacts produced from this repository.

Out of scope:

- Third-party dependencies (please report those upstream).
- Social engineering, physical attacks, or denial-of-service testing.
- Automated scanner output without a demonstrated impact.

## Safe Harbor

We will not pursue or support legal action against researchers who:

- Make a good-faith effort to comply with this policy.
- Avoid privacy violations, data destruction, and service disruption.
- Give us reasonable time to remediate before public disclosure.

## Credit

With your permission, we will credit you in the release notes or security
advisory that accompanies the fix. Let us know in your report if you would
prefer to remain anonymous.
