# Network Security: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. You are handed a 4 GB pcap from a workstation from "something weird last week." The analyst who requested the review is already impatient. Where do you start and why?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not open the full pcap and scroll: starts with statistics and protocol breakdown
- Uses conversation view to identify top talkers and unusual endpoints
- Filters for external destinations first, especially unexpected ports or IPs
- Looks for DNS queries to unusual domains or high-entropy names
- Checks for large data transfers or sustained beaconing patterns
- Asks what "weird" means before diving in, to prioritize search direction
- Identifies what timeframe is most relevant based on the incident report

</details>

## Mid-Level

### Q1. A backend service started sending traffic to an unknown external IP on port 443 three days ago. Netflow is the only telemetry you have: no pcap, no endpoint agent. Walk through what you can and cannot conclude, and what you ask for next.

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Lists what Netflow does give: source/dest IP, port, bytes, duration, frequency
- Lists what Netflow does not give: payload, process name, user context, certificate details
- Checks for beaconing patterns in timing intervals
- Looks up the destination IP in threat intel and passive DNS
- Identifies which host originated the traffic to request endpoint telemetry
- Does not conclude compromise without additional evidence
- Asks for firewall logs, DNS logs, and endpoint process data as next steps
- Considers legitimate explanations before assuming malicious intent

</details>

## Senior / Advanced

### Q1. You are asked to design network segmentation for a hospital that has corporate workstations, clinical devices running legacy Windows, medical IoT (infusion pumps, imaging machines), and guest Wi-Fi. The CIO wants "zero trust." How do you translate that into something deployable in a hospital?

*Difficulty: ⭐⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Acknowledges that "zero trust" is an architecture philosophy, not a product
- Segments clinical devices on isolated VLANs due to inability to patch or agent
- Designs clinical network for minimal blast radius: no lateral movement paths to corporate
- Identifies that medical devices often cannot support endpoint agents or certificate auth
- Proposes network-level controls (NAC, port security) where agent-based controls fail
- Addresses guest Wi-Fi isolation as baseline, not a zero-trust initiative
- Raises clinical workflow impact: a nurse cannot be locked out during a patient emergency
- Sequences the rollout by risk tier rather than attempting all segments simultaneously
- Involves clinical engineering and compliance in the design, not just IT security

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
