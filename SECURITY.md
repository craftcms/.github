# Security Policy

## Products Covered

This security policy covers Craft CMS, Craft Commerce, Craft Cloud, and Pixel & Tonic 1st-party plugins.

## Reporting a Vulnerability

If you discover a security vulnerability, please review these guidelines before submitting a report. We take security seriously and do our best to resolve security issues as quickly as possible.

## Guidelines

While working to identify potential security vulnerabilities, we ask that you:

- Share any issues you discover with us via [our website](https://craftcms.com/contact), support@craftcms.com, or support@craft.cloud as soon as possible.
- Give us reasonable time to address and release any fixes for reported issues before publicizing them. Preferably 30 days.
- Only report issues [in scope](#scope).
- Provide a quality report with precise explanations and concrete attack scenarios.
- Ensure you’re aware of the versions of Craft CMS and Craft Commerce that are actively [receiving security fixes](https://craftcms.com/knowledge-base/supported-versions). Craft Cloud is always open to receive security fixes.

## Scope

### Craft CMS, Craft Commerce, and plugins

We are interested in vulnerabilities that affect Craft or [first-party Craft plugins](https://github.com/craftcms), tested against **your local installation of the software**. You can install a local copy of Craft by following these [installation instructions](https://craftcms.com/docs/installing). Do **not** test against any Craft installation you don’t own, including [craftcms.com](https://craftcms.com).

### Craft Cloud

We are interested in infrastructure-related vulnerabilities found on Craft Cloud.

Do **not** test against any Craft Cloud site you don’t own, and do **not** perform any tests that degrade the Craft Cloud’s services.

We are only interested in reports directly from the security researcher who discovered them, not from third-party bug bounty programs.

### Qualifying Vulnerabilities

- [Cross-Site Scripting (XSS)](https://en.wikipedia.org/wiki/Cross-site_scripting)
- [Cross-Site Request Forgery (CSRF)](https://en.wikipedia.org/wiki/Cross-site_request_forgery)
- [Arbitrary Code Execution](https://en.wikipedia.org/wiki/Arbitrary_code_execution)
- [Privilege Escalation](https://en.wikipedia.org/wiki/Privilege_escalation)
- [SQL Injection](https://en.wikipedia.org/wiki/SQL_injection)
- [Session Hijacking](https://en.wikipedia.org/wiki/Session_hijacking)

### Non-Qualifying Vulnerabilities

- Reports from automated tools or scanners
- Theoretical attacks without proof of exploitability
- Attacks that can be guarded against by following our [security recommendations](https://craftcms.com/knowledge-base/securing-craft).
- Server configuration issues outside of Craft’s control
- [Denial of Service](https://en.wikipedia.org/wiki/Denial-of-service_attack) attacks
- [Brute force attacks](https://en.wikipedia.org/wiki/Brute-force_attack) (e.g. on password or token hashes)
- Username or email address enumeration
- Social engineering of Pixel & Tonic staff or users of Craft installations
- Physical attacks against Craft installations
- Attacks involving physical access to a user’s device or involving a device or network that’s already seriously compromised (e.g. [man-in-the-middle attacks](https://en.wikipedia.org/wiki/Man-in-the-middle_attack))
- Attacks that are the result of a third-party Craft plugin should be reported to the plugin’s author
- Attacks that are the result of a third-party library should be reported to the library maintainers
- Bugs that rely on unlikely user interactions (i.e., the user effectively attacking themselves)
- Disclosure of tools or libraries used by Craft and/or their versions
- Issues that are the result of a user ignoring common security best practices (like sharing their password publicly)
- Missing security headers that do not lead directly to a vulnerability via proof of concept
- Vulnerabilities affecting users of outdated/unsupported browsers or platforms
- Vulnerabilities affecting outdated versions of Craft
- Any behavior that is clearly documented
- Issues discovered while scanning a site you don’t own without permission
- Missing CSRF tokens on forms (unless you have a proof of concept, many forms either don’t need CSRF or are mitigated in other ways) and “logout” CSRF attacks
- [Open redirects](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html)

## Bounties

We’re happy to offer researchers a monetary reward to show our appreciation for the work it can take to find and report a vulnerability.

Reward amounts vary depending on the severity. Our minimum reward for a qualifying vulnerability report is $50 USD, and we expect to pay $500+ USD for significant vulnerabilities.

A report will qualify for a bounty if:

- Our [Guidelines](#guidelines) have been followed in full.
- The vulnerability was previously unknown to us, or your report provides more information or shows the vulnerability to be more extensive than we initially thought.
- The vulnerability is non-trivial.
