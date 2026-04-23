# SOC Analyst: Interview Questions

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

### Q1. You're reviewing firewall logs and see outbound traffic from a workstation to port 443 on an external IP. Your junior colleague says "That's just HTTPS, it's fine." But you notice the destination IP has no reverse DNS and the traffic volume is unusually high. What's your thinking process?

*Difficulty: ⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Knows 443 is HTTPS but that doesn't automatically mean legitimate
- Standard port can hide malicious traffic (C2 over HTTPS is common)
- No reverse DNS could indicate attacker infrastructure
- High volume could be data exfiltration, not normal browsing
- Would check if the IP is in threat intel feeds
- Would look at the workstation for signs of compromise
- Understanding ports helps triage, but context matters more
- "It's a common port" is not a reason to close an alert

</details>

---

## Mid-Level

### Q1. Your SIEM fires a high-confidence alert: PowerShell spawned by Microsoft Word. You confirm it fired on a legitimate finance user opening an Excel macro for a monthly report. Walk me through what you do in the moment, and what you do afterward to avoid this becoming a noisy rule.

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not immediately close as false positive without investigation
- Verifies the macro source and confirms it is a known, controlled file
- Documents the legitimate use case before tuning
- Proposes allowlisting by specific parent process hash or file path, not broad rule suppression
- Considers whether the macro itself should be reviewed or sandboxed
- Creates a process to re-evaluate the tuning if the macro changes
- Communicates the decision and rationale to the team

</details>

---

## Senior / Advanced

### Q1. You take over a SOC that produces 40,000 alerts per month, 70% of which close as false positive. Leadership is proud because "we catch everything." What is broken, and what is your 90-day plan?

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies alert fatigue as a threat: analysts stop reading alerts carefully
- Distinguishes between detection coverage and detection quality
- Audits the top 10 noisiest rules first for tuning or retirement
- Establishes signal-to-noise metrics (MTTD, false positive rate per rule)
- Segments alerts by confidence and fidelity, not just severity
- Involves analysts in tuning rather than top-down rule changes
- Sets a target false positive rate and tracks it weekly
- Does not propose silencing rules without understanding root cause first
- Communicates to leadership why "catching everything" can be counterproductive

</details>

---

## All Levels

### Q1. You are on call when an alert fires at 2am for anomalous Linux process behavior. You log in and quickly realize the alert is almost certainly a false positive. Walk me through your thought process: do you dismiss it, and how do you handle it in a way that improves the program rather than just closing a ticket?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: behavioral*

<details>
<summary>What a strong answer covers</summary>

- Does not dismiss the alert without documenting the reason: false positive handling must be recorded to enable tuning
- Investigates sufficiently to be confident it is a false positive rather than assuming based on superficial inspection
- Files a tuning request or adjusts the rule rather than accepting repeated false positives as inevitable
- Recognizes that a high false positive rate degrades the entire detection program by reducing analyst trust in alerts
- Considers whether the false positive reveals a detection logic flaw that could also produce false negatives

</details>

---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
