# GRC / Compliance: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)
- [All Levels](#all-levels)

---

## Junior / Entry-Level

### Q1. Your engineering team checked a database dump into a public GitHub repo. It contains customer emails and hashed passwords. Nothing is formally classified in your organization. What does this incident reveal about your data governance, and what would you propose to prevent it?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies the root cause: no data classification means engineers do not know what is sensitive
- Notes that hashed passwords are still regulated data under most privacy laws
- Addresses the immediate response: assess exposure, notify legal, check if repo was indexed
- Proposes a data classification policy as the foundational fix
- Suggests developer training on what constitutes sensitive data
- Recommends technical controls: pre-commit hooks, secret scanning in CI/CD
- Does not rely solely on policy without technical enforcement

</details>

## Mid-Level

### Q1. You discover that customer support has been exporting full customer records to shared Google Sheets to make lookups easier, going back three years. Walk through what went wrong at each stage of the data lifecycle and how you address each.

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Creation/collection: no data minimization, full records exported when partial would suffice
- Storage: uncontrolled third-party storage, outside approved systems of record
- Use: no access controls, sheets shared broadly without need-to-know
- Retention: three years of data with no deletion or review process
- Disposal: no process to clean up the sheets now discovered
- Addresses the human side: support team was solving a real usability problem, fix the root cause
- Proposes a remediation plan that does not just say "stop doing it"
- Considers regulatory notification obligations depending on jurisdiction

</details>

## Senior / Advanced

### Q1. You're building an enterprise data classification program from scratch. Walk me through your approach.

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Executive sponsorship and governance committee formation
- Define classification levels aligned with business and regulatory needs
- Establish roles: data owners, stewards, custodians per business unit
- Policy development with clear handling requirements per level
- Data discovery and inventory across all systems
- Pilot with one business unit, refine based on feedback
- Deploy automated classification tools (DLP, CASB, cloud-native)
- Training program for all employees
- Integration with access control and DLP systems
- Metrics: classification coverage, policy violations, time to classify
- Annual review and update cycle

</details>

## All Levels

### Q1. A new SRE asks for the same break-glass admin role that everyone else on the team has, "because it is easier and we all trust each other." How do you respond, and what do you offer instead?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not dismiss the request as obviously wrong: acknowledges the operational need
- Explains why "we trust each other" does not address audit, insider threat, or compromise scenarios
- Proposes a just-in-time access model: request elevated access when needed, auto-expire
- Distinguishes between standing access and break-glass access
- Offers a practical alternative that does not slow down legitimate work
- Raises the accountability problem: shared admin actions are harder to attribute
- Notes that if everyone has admin, it is no longer "break-glass"

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
