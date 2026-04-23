# Identity & Access Management: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. A user successfully logs in with their password but can't access a financial report they need for their job. When you check the logs, there's no record of them even trying to access it. Walk me through how you'd troubleshoot this and what each step tells you.

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Recognizes this involves all three AAA components
- Authentication worked: User proved identity via password
- Authorization issue: Check if user/role has permission to that resource
- Accounting gap: Why no log entry? Is logging configured for that resource?
- Would check group memberships, role assignments, resource permissions
- Would verify logging is enabled and functioning for that system
- Considers whether the resource path/URL is even correct

</details>

## Mid-Level

### Q1. An executive loses their phone and laptop while traveling internationally. They have hardware MFA tokens but left them at home. They need access to approve an urgent contract. How do you verify their identity and provide secure emergency access without undermining your authentication controls?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Takes identity verification seriously - can't just reset because they say it's urgent
- Uses pre-established out-of-band verification (security questions, video call with known colleague)
- Doesn't disable MFA - provides alternative temporary authentication
- Options: Temporary access code via verified phone call, one-time bypass with heavy audit
- Documents the exception with business justification
- Access should be temporary and limited to specific need (contract approval)
- Immediately revokes any bypass after the action is completed
- Investigates lost devices - were they compromised? Remote wipe if possible
- This scenario should trigger review of emergency access procedures
- Executive should have documented recovery options before traveling

</details>

## Senior / Advanced

### Q1. You are tasked with rolling out passwordless authentication to 8,000 employees across corporate headquarters, a call center with shared workstations, and field technicians who use personal phones. The CIO wants one solution. Walk me through why that is wrong and how you structure the rollout.

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies that each group has different device posture and authentication constraints
- HQ workers: FIDO2 hardware keys or platform authenticators on managed devices
- Call center shared workstations: hardware tokens or smart cards; passkeys do not work on shared machines tied to individual accounts
- Field technicians on personal phones: FIDO2 or push-based auth with device trust challenges for unmanaged devices
- Raises that "one solution" optimizes for procurement simplicity, not security or usability
- Identifies the call center as the hardest problem: shared device authentication is a known unsolved challenge
- Proposes a phased rollout by segment with different controls per group
- Defines success metrics: phishing simulation pass rates, helpdesk ticket reduction, not just deployment percentage

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
