# Security Policy

The SciCat project takes security seriously. This file documents the general security
procedures for SciCatProject repositories. Individual repositories may have additional
information in their own `SECURITY.md` files.

## Reporting a Vulnerability

If you believe you have found a security vulnerability in SciCat, please report it
privately via one of the following:

- ✅ Create a **private security advisory** using the 'Report a vulnerability' button in
  the 'Security and quality' tab or by going to
  `https://github.com/SciCatProject/<repo>/security/advisories/new`.
- ✅ Email the project leaders:
  [scicat-leaders@lists.psi.ch](mailto:scicat-leaders@lists.psi.ch)
- ✅ Notify a project leader by *Direct Message* in the [scicat slack
  chat](https://join.slack.com/t/scicat/shared_invite/zt-251efp7t2-8IqFDo3sPN8TYWgKNywccg).
  Check the [website](https://www.scicatproject.org/) for current project leaders.
- ❌ DO NOT report security vulnerabilities through public GitHub issues, discussions, or
  pull requests, public slack channels, etc.

Please include as much information as you can to help us better understand and resolve
the issue. We will work on fixing the issues
[privately](https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/collaborating-in-a-temporary-private-fork-to-resolve-a-repository-security-vulnerability).

## Disclosure

Serious vulnerabilities are announced confidentially to cybersecurity personal and
select SciCat operators ahead of the public disclosure to allow organizations time to
patch public systems. Please [contact the project
leaders](mailto:scicat-leaders@lists.psi.ch) if you would like to be notified about
security advisories prior to the public disclosure.

We use GitHub [security
advisories](https://github.com/SciCatProject/scicat-backend-next/security/advisories) to
disclose vulnerabilities publicly after a fix is available.

## Responding to a vulnerability

This section is intended for SciCat developers responding to a new security advisory.

1. Project Leaders (PL) will triage the vulnerability and assign developers to start
   working on a fix.
   1. Create a private security advisory, if the reporter did not already.
   2. Grant the team `@SciCatProject/security` access to the advisory
   3. Declare a code freeze to reduce conflicts until the vulnerability is patched
2. PL notify the security team privately about the vulnerability. Include information
   about the expected time to a fix. Facilities should be prepared to update promptly
   when the patch is released. Private communication channels include:
    - [scicat-security@lists.psi.ch](https://psilists.ethz.ch/sympa/subscribe/scicat-security)
      (including Steering Committee members)
    - `#security` slack channel
    - [Security](https://github.com/orgs/SciCatProject/teams/security) Github Team
3. From the advisory, create a private fork to collaborate.
    1. Develop on the `master` and `release` branches directly. Pull requests from the
       private fork must match branch names from the upstream repository.
    2. Keep the fix minimal and don't incorporate additional features. Squash commits
       regularly to make it easy to cherry-pick.
    3. Cherry-pick the fix to `master`, `release` (and long-term releases, if
       applicable)
    4. Create PRs to back to the upstream repo for review.
4. Operators have 1-2 days to review the fix & prepare (privately) for the upgrade. If
   they run a fork, they should cherry-pick the fix onto their deployed branch.
5. Draft an email announcement and release notes in preparation for the patch release
6. When the fix is ready:
    1. Merge all PRs. This is an atomic step.
    2. Immediately make a patch release from the `release` branch
    3. Send the email announcement with information
7. Facilities update to the new release or master branch.
8. The next scicat operator meeting should include a retrospective analyzing the
   incident response.
