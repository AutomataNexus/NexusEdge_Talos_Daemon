# Security Policy

## Supported Versions

| Version | Supported          |
|---------|--------------------|
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

**DO NOT open a public GitHub issue for security vulnerabilities.**

Please report security vulnerabilities privately via email:

**Email:** security@automatanexus.com
**PGP:** Available on request
**Response time:** We aim to acknowledge within 24 hours and provide a fix timeline within 72 hours.

### What to include

- Description of the vulnerability
- Steps to reproduce
- Affected version(s)
- Potential impact assessment
- Suggested fix (if any)

### What qualifies

- Authentication bypass
- Privilege escalation (viewer → admin, community → pro)
- AI safety guardrail bypass (Sage jailbreak, prompt injection)
- Credential exposure (vault contents, API keys, SMTP credentials)
- Remote code execution
- Control output manipulation via AI or API
- License/subscription bypass
- Cross-tenant data access in the portal

### What does NOT qualify

- Denial of service against a local controller (physical access required)
- Issues requiring physical access to the Raspberry Pi
- Theoretical attacks with no proof of concept
- Issues in third-party dependencies (report to the upstream project)

### Disclosure Policy

- We follow coordinated disclosure — we will credit reporters (unless anonymity is requested) and publish advisories after fixes are available.
- We will not take legal action against researchers acting in good faith.

### Bug Bounty

We do not currently operate a formal bug bounty program, but we recognize and credit responsible disclosures in our release notes.

---

AutomataNexus LLC — Wolcottville, Indiana 46795, USA
