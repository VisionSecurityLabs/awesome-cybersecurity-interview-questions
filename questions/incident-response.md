# Incident Response / DFIR: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. A user calls the help desk saying their laptop is "running weird" and they think it might be infected. The laptop is still on, connected to corporate VPN, and the user is standing in front of it. What do you do in the first five minutes, and why in that order?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not immediately reboot or power off: volatile memory and active connections have forensic value
- Disconnects from VPN first to limit lateral movement risk while keeping the machine on
- Takes a screenshot or photo of the current state before touching anything
- Asks the user what they were doing when they noticed the issue and whether they clicked anything
- Notes the time and documents initial observations before proceeding
- Decides whether to escalate to full IR or handle at the help desk level based on initial indicators
- Does not run antivirus immediately: it may overwrite forensic artifacts
- Knows when to stop and hand off to a more experienced responder

</details>

## Mid-Level

### Q1. Your public-facing web application is experiencing a volumetric DDoS attack. Customer-facing services are down. Walk through your response.

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Engage DDoS mitigation service/provider immediately
- Enable rate limiting at edge/WAF
- Analyze attack traffic patterns (source IPs, request types)
- Activate geo-blocking if attack sourced from specific regions
- Scale infrastructure if cloud-based
- Communicate with stakeholders about service impact
- Consider null-routing specific IP ranges
- Document attack metrics for post-incident analysis

</details>

## Senior / Advanced

### Q1. Your organization receives an alert that a software vendor you use has been compromised and is distributing malware through their legitimate update channel. Walk through your response.

*Difficulty: ⭐⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identify all systems running the affected software
- Check version numbers against compromised versions
- Network isolate affected systems immediately
- Block update servers at firewall/proxy
- Analyze for IOCs associated with the campaign
- Check for lateral movement from affected systems
- Engage vendor for official remediation guidance
- Coordinate with industry ISACs for shared intelligence

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
