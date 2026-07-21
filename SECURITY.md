# Security

The security of Craft CMS, Craft Commerce, Craft Cloud, and all Pixel & Tonic plugins is of the utmost importance to us, our community, and our customers.

We strive to ensure the integrity of our software and infrastructure and to have processes in place to address all security issues in a timely manner while minimizing customer exposure.

## Overview

Craft CMS is a self-hosted PHP web application. It is important for developers, administrators, and customers to realize it is not a “shrink-wrapped” solution and that every site is 100% unique and custom-built. Because of this, we do not have access to the infrastructure a self-hosted Craft is installed on, or even knowledge of where it is hosted.

From a security perspective, we are primarily concerned with issues that arise from a fresh Craft installation, not any front-end site implementation or custom plugins or modules, unless they reveal a foundational issue that can be addressed in Craft’s native code across all installations.

## Patches and Updates

The most secure version of Craft or Commerce is the latest one.

If you’re on a version of Craft or Commerce that is no longer being [actively supported](https://craftcms.com/knowledge-base/supported-versions), you should update to a supported version.

Even if you are on a supported version, you should make sure you are running the latest release to ensure you have the latest security patches and bug fixes.

# Vulnerability Disclosure

We triage, acknowledge, patch, and disclose any vulnerabilities in an industry-standard manner.

If you believe you have discovered a potential security vulnerability in our products, please report your findings to us as quickly as possible.

## Reporting a Vulnerability

If you discover a security vulnerability, please review these guidelines before submitting a report. We take security seriously and do our best to resolve security issues as quickly and responsibly as possible.

## Guidelines

While working to identify potential security vulnerabilities, we ask that you:


* Share any issues you discover with us via our Vulnerability Disclosure Program on Hackrate at [https://www.hckrt.com/Reports/EmbeddedReportForm?program=craftcms-vdp](https://www.hckrt.com/Reports/EmbeddedReportForm?program=craftcms-vdp)
* Give us a reasonable amount of time to address and release any fixes for reported issues. We publicly disclose issues 30 days after a release that includes a fix.
* Only report issues [in scope](#scope).
* Provide a quality report with precise explanations, concrete attack scenarios, and the steps to follow to reproduce the issue. Attachments such as screenshots or proof-of-concept code are highly recommended.
* Ensure you’re aware of the versions of Craft CMS and Craft Commerce that are actively [receiving security fixes](https://craftcms.com/knowledge-base/supported-versions). Craft Cloud is always open to receive security fixes.
* Test against authorized targets at Hackrate.
* Avoid privacy violations, destruction of data, and interruption or degradation of Craft CMS’s services.
* Only interact with accounts you own.
* Rewards or recognition will not be awarded if our security team cannot reproduce and verify a finding.
* You must be the first person to report a valid finding.
* If you find the same vulnerability several times, report only one finding. Multiple vulnerabilities caused by a single underlying issue will be considered a single report.

## Triage & Collaboration

Once an issue has been reported, we will attempt to replicate it locally, on the latest release of Craft or Commerce. We might ask follow-up questions depending on the report.

We manage all of our security advisories and reports through our VDP at [Hackrate](https://www.hckrt.com).

If it is accepted, we will also publish a GitHub Security Advisory in the [the](https://github.com/craftcms/cms/security) [respective](https://github.com/craftcms/commerce/security) [repository](https://github.com/craftcms/cloud/security).

You can see an up-to-date list of known/fixed security issues in those repositories, and those should be considered the “source of truth” for security issues.

We may ask you to verify the fix during the collaboration process.

## Disclosure Timeline

We wait 30 days _after the Craft or Commerce release_ that has a fix before we make the security advisory public. This is to give customers time to update before any details are made public. We ask that the reporters not disclose any information about the vulnerability until that 30-day window is up and it is made public.

## Scope

We are only interested in reports directly from the security researcher who discovered them.

### Craft CMS, Craft Commerce, and plugins

We are interested in vulnerabilities that affect Craft or [first-party Craft plugins](https://github.com/craftcms), tested against **your local installation of the software**. You can install a local copy of Craft by following these [installation instructions](https://craftcms.com/docs/installing). Do **not** test against any Craft installation you don’t own, including [craftcms.com](https://craftcms.com).

### Craft Cloud

We are interested in infrastructure-related vulnerabilities found on Craft Cloud.

Do **not** test against any Craft Cloud site you don’t own, and do **not** perform any tests that degrade Craft Cloud’s services.

### Non-Qualifying Vulnerabilities

Avoid reporting vulnerabilities that meet the following criteria:

* Reports from automated tools or scanners
* Theoretical attacks, direct or in a chain, without proof of exploitability
* Attacks that can be guarded against by following our [security recommendations](https://craftcms.com/knowledge-base/securing-craft).
* Server configuration issues outside of Craft’s control
* [Denial of Service](https://en.wikipedia.org/wiki/Denial-of-service_attack) attacks
* [Brute force attacks](https://en.wikipedia.org/wiki/Brute-force_attack) (e.g., on password or token hashes)
* Username or email address enumeration
* Social engineering of Pixel & Tonic staff or users of Craft installations
* Physical attacks against Craft installations
* Attacks involving physical access to a user’s device or involving a device or network that’s already seriously compromised (e.g., [man-in-the-middle attacks](https://en.wikipedia.org/wiki/Man-in-the-middle_attack))
* Attacks that are the result of a third-party Craft plugin should be reported to the plugin’s author
* Attacks that are the result of a third-party library should be reported to the library maintainers
* Bugs that rely on unlikely user interactions (i.e., the user effectively attacking themselves)
* Disclosure of tools or libraries used by Craft and/or their versions
* Issues that are the result of a user ignoring common security best practices (like sharing their password publicly)
* Missing security headers that do not lead directly to a vulnerability via proof of concept
* Vulnerabilities affecting users of outdated/unsupported browsers or platforms
* Vulnerabilities affecting outdated versions of Craft
* Any behavior that is clearly documented
* Issues discovered while scanning a site you don’t own without permission
* Missing CSRF tokens on forms (unless you have a proof of concept, many forms either don’t need CSRF or are mitigated in other ways) and “logout” CSRF attacks
* Reports of insecure SSL/TLS ciphers
* Homograph attacks
* Password and account recovery policies, such as reset link expiration or password complexity
* Disclosure of known public files or directories
* Errors thrown by web services (e.g., nginx) when the requests are invalid / fuzzing
* HttpOnly and Secure cookie flags, as well as other missing cookie flags
* Missing security-related HTTP headers, which do not lead directly to a vulnerability
* Massive automated actions on the platform through robots/crawling
* RTLO and related issues
* Invalid or missing SPF records (e.g., incomplete or missing SPF/DKIM/DMARC)
* [Open redirects](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html)
* XSS attacks that do not directly lead to a more foundational threat (e.g., privilege escalation)
* Already [known](https://github.com/craftcms/cms/security/advisories) [issues](https://github.com/craftcms/commerce/security/advisories).

#### Elevated Sessions

* Elevated sessions are intended as an extra layer of protection against **long-term** privilege escalation, in the event that a session has been hijacked. We are not interested in reports related to elevated sessions, outside of that context.

## Severity & Remediation

We assign the broader severity categories of **Critical**, **High**, **Moderate**, and **Low**.

**Critical:** There is a very high chance of compromise for affected sites. Typically, these are through untrusted or unauthenticated users, and there may already be active exploits in the wild targeting vulnerable sites.

**High:** Poses a potential security threat to the underlying installation, although the flaw is usually difficult to exploit.

**Moderate:** Typically requires local network or user privileges to be exploited first, though not necessarily. The impact on business operations is slightly higher. The flaw is usually difficult to exploit.

**Low:** Most XSS vulnerabilities. Most denial of service vulnerabilities. They typically do not compromise the underlying data or system and don’t pose a risk of privilege escalation, arbitrary code execution, or data loss. Or if they do, but they have to go against our [security recommendations](https://craftcms.com/knowledge-base/securing-craft) to achieve it (e.g., `allowAdminChanges` enabled in production).

---

As a rule of thumb, here are some guidelines on when customers should update, depending on the severity level.

| Critical| High| Moderate| Low|
|---|---|---|---|
| Update ASAP| Update within 30 days| Update within 90 days (depending on your site’s needs)| Update at your convenience (depending on your site’s needs) |
