# Threat Intelligence: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. Your threat intel team just published a report on a new ransomware group. The CISO wants a 1-page executive summary, the SOC wants detection rules, and the IR team wants incident playbook updates. How do you tailor the same intelligence for these three different audiences?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Recognizes different audiences need different formats and depth
- CISO: Business impact, likelihood for our sector, recommended investments
- SOC: IOCs, detection signatures, ATT&CK techniques to monitor
- IR: Response procedures, containment strategies, recovery timeline
- Focuses on "so what" and actionable recommendations for each
- Prioritizes IOC delivery to SOC given short shelf life vs. strategic briefing to CISO

</details>

## Mid-Level

### Q1. A colleague says you should immediately push all IOCs from a new vendor feed into blocking mode to "get value right away." Why is that wrong, and how do you actually onboard a new intel feed?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies the risk: blocking on unvalidated IOCs causes false positives and business disruption
- Proposes a staged onboarding: alert-only mode first, then blocking after validating fidelity
- Establishes a baseline false positive rate before deciding on blocking posture
- Checks IOC age and source confidence before any action: stale or low-confidence IOCs degrade detection quality
- Segments IOC types: IPs rotate fast and have high false positive rates; domains and hashes are more stable
- Reviews overlap with existing feeds to assess the vendor's actual additive value
- Sets a review period to evaluate the feed's performance before renewing or expanding

</details>

## Senior / Advanced

### Q1. You work at a mid-sized regional bank. Leadership has read that "AI-powered ransomware" is the top threat for next year and wants you to focus your threat assessment there. How do you produce an honest 12-month threat assessment, and how do you handle the fact that leadership has already decided what they want to hear?

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not simply validate the narrative: uses threat intelligence methodology to assess actual likelihood and impact for a regional bank
- Starts from threat actor profiling: who actually targets regional banks and why
- Grounds the assessment in the organization's specific attack surface and crown jewels, not industry headlines
- Addresses AI-powered ransomware honestly: if the evidence supports it, include it; if not, explain why it ranks lower than more proven threats
- Prepares to present findings that may contradict the expectation, with evidence to support the conclusion
- Structures the briefing so leadership can understand the methodology, not just the conclusion
- Does not bury the lead to avoid conflict: states clearly where the assessment diverges from the assumption and why
- Offers to revisit if new evidence emerges rather than committing to a fixed narrative

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
