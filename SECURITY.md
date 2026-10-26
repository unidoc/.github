# Security Policy

This policy applies to every repository in the unidoc ([https://github.com/unidoc](https://github.com/unidoc)) organisation, to our websites and to our hosted services more about how we work is at [https://security.unidoc.io](https://security.unidoc.io). 

Our libraries parse PDF, Office and HTML files, and that input is usually untrusted, so a parsing bug is reachable by anyone who can get a document into a customer's pipeline. Malformed and hostile files are the core of this policy, not an edge case.

## Reporting a vulnerability

**Please do not report vulnerabilities through public issues, pull requests or
discussions.**

Use [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability)
— open the **Security** tab of the affected repository and click **"Report a
vulnerability"** — or email **[security@unidoc.io](mailto:security@unidoc.io)** if you
cannot use GitHub reporting.

Please include what you know:

- the affected product and version, or commit;
- the operating system and architecture;
- the API call or command involved, and any relevant configuration;
- a minimal reproducer or input file, if you can share one;
- the impact you observed, and any mitigation you have identified;
- whether the issue is already public, with links;
- whether you suspect exploitation outside testing, and when you saw it.

Incomplete reports are welcome. If you suspect active exploitation, say so in the
subject line or the first sentence.

Please do not send passwords, private keys or confidential customer documents.
Describe sensitive evidence first and we will agree a transfer method. If you need an
encrypted channel, ask in your first message.

## Response and assessment

Measured from when we receive your report:

| Stage | Our target |
| --- | --- |
| We acknowledge your report | within **3 business days** |
| We send you a first assessment | within **10 business days** |
| We update you while work continues | at least every **14 calendar days** after the first assessment |

**These are communication targets, not guaranteed resolution times**, and they are the
same for everyone — you do not need to be a customer to receive them. If you have not
heard from us within the target period, please follow up. If we are going to miss a
target, we will say so with a revised estimate rather than go quiet.

Security fixes for supported versions are free of charge for everyone, whether or not
you hold a commercial licence. A commercial licence additionally provides support and  
maintenance under the applicable agreement and SLA, including response times for  
support requests, delivery of fixes, maintenance of supported versions, and direct  
communication with our engineering team, on the agreed  
[terms and service levels](https://unidoc.io/sla/).

We credit you in the advisory unless you would rather not be named.

## Scope

This policy covers vulnerabilities affecting software and services developed,
maintained, distributed or operated by UniDoc, including:

- **Source code and repositories** — repositories maintained under the UniDoc
organisation, including UniDoc-specific modifications to third-party projects.
- **Distributed software** — vulnerabilities in UniDoc libraries, binaries, container
images and other released artifacts, including third-party components bundled with
or distributed as part of our products.
- **Websites and hosted services** — websites, APIs, licensing services and other
infrastructure operated by UniDoc.
- **Build and release infrastructure** — CI/CD systems and release pipelines, where a
vulnerability could compromise the integrity or authenticity of what we publish.
- **Document processing** — vulnerabilities triggered by malformed or malicious PDF,
Office, HTML or other supported input, including issues leading to code execution,
unauthorised access, information disclosure or denial of service.

### Out of scope

- Third-party tools we invoke but do not ship — please report those to their
maintainers.
- Issues in an upstream project we merely keep a fork of. Several repositories here  
are forks we maintain so that a UniDoc product can depend on them report those  
upstream first, and tell us as well if the issue changes how the fork behaves inside  
one of our products.
- Findings our own tools (UniSupply, gorisk.dev) report against third-party code,
which belong to that upstream project.
- Scanner output with no demonstrated impact.
- Denial of service against our websites by traffic volume alone.
- Social engineering of our staff, and physical attacks.
- Third-party services we use but do not operate.

## Supported versions

Security fixes are provided for the version lines below. Where a product is still
pre-1.0, each new minor release may change the API, so support tracks the latest
release rather than a major line. Release notes in each repository describe any
changes an upgrade requires.

| Product | Licence | Versions receiving security fixes |
| --- | --- | --- |
| UniPDF | Commercial (EULA) | `v5.x` |
| UniOffice | Commercial (EULA) | `v2.x` |
| UniHTML | Commercial (EULA) | latest release |
| UniPDF-CLI | Commercial (EULA) | latest release |
| UniType | Commercial (EULA) | latest release |
| UniChart | MIT | latest release |
| UniSupply | Apache-2.0 | latest release |
| ISMS | Apache-2.0 | latest release |
| PDF Debugger | Apache-2.0 | latest release |

If you need a security fix for an older version line, contact us at [security@unidoc.io](mailto:security@unidoc.io). We only support the latest lines, but we can look at requests case by case.  
Hosted services — unidoc.io, isms.sh, gorisk.dev, the licensing API at cloud.unidoc.io, and the UniHTML rendering server — are supported at the version currently deployed or published.

## Coordinated disclosure

1. You report privately through one of the channels above.
2. We acknowledge, assess, and agree a timeline with you.
3. We prepare the fix in a private advisory.
4. We request a CVE where appropriate.
5. We release the fix, publish the advisory, and credit you.

We ask you to allow reasonable time for us to investigate and fix a reported  
vulnerability before publishing technical details we will agree a disclosure date  
with you rather than leave one open.

We do not require an NDA to report a vulnerability, and we will not pursue legal
action against good-faith security research conducted within this policy's scope.

We keep reports confidential and share details only as far as investigation,
remediation, coordination and legal reporting require.

## Actively exploited vulnerabilities

If a vulnerability in one of our products is ever actively exploited, we follow the  
reporting obligations of the EU Cyber Resilience Act and tell affected customers what  
they need to do. Regulatory notification is handled separately from publication of the  
public advisory, and is not delayed to meet a preferred disclosure date.
