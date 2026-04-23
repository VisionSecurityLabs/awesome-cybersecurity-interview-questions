# Application Security: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. A developer shows you a new internal API they built in an afternoon. Auth is a static API key in the Authorization header, it returns full user objects including hashed passwords "because the frontend needs them," and there is no rate limit because "it is internal only." What do you raise first, and why?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Prioritizes the data exposure issue: returning hashed passwords is unnecessary and a breach risk
- Questions the "internal only" assumption: internal APIs get called by compromised hosts and misconfigured services
- Raises that static API keys do not expire, cannot be scoped, and are easy to leak in logs
- Notes missing rate limiting enables credential stuffing and abuse even internally
- Does not try to fix everything at once: identifies the highest-risk issue first
- Asks what "the frontend needs" actually requires vs. what is being returned
- Proposes data minimization as the fix for the response payload, not just access control

</details>

## Mid-Level

### Q1. A team is building three clients against the same API: a server-rendered web app, a mobile app, and a cron job that syncs data overnight. They want to use one OAuth flow for simplicity. Why is that wrong, and how do you guide them?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies that each client has different trust characteristics and risk profiles
- Web app with backend: Authorization Code flow, server holds tokens securely
- Mobile app (public client): Authorization Code with PKCE, no client secret
- Cron job (machine-to-machine, no user): Client Credentials, service identity not user identity
- Explains why a single flow fails at least one client: PKCE is wrong for M2M, Client Credentials is wrong for user-facing apps
- Raises that "simplicity" in auth often introduces vulnerability
- Notes the team can still use the same authorization server, just different grant types per client

</details>

## Senior / Advanced

### Q1. Design an API security program for an organization with 200+ microservices and multiple API products.

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Governance: API security standards, review process, ownership model
- Inventory: API catalog, classification by sensitivity, lifecycle tracking
- Design standards: security requirements by API type (internal/partner/public)
- Authentication framework: centralized identity, token standards
- API gateway: enforce policies consistently, single pane of glass
- Security testing: SAST/DAST in pipeline, manual review for sensitive APIs
- Monitoring: anomaly detection, abuse patterns, security metrics
- Incident response: API-specific playbooks, quick key revocation
- Developer training: secure API development curriculum
- Third-party risk: partner security requirements, integration reviews
- Compliance: PCI-DSS API requirements, audit readiness

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
