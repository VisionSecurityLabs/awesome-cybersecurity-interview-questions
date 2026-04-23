# OT / ICS Security: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. The IT security team wants to implement their standard monthly patch cycle on your manufacturing plant's control systems. They propose scheduling automatic Windows updates for Sunday at 2 AM "when no one is working." As the OT security engineer, how do you respond to this proposal and what alternative approach do you recommend?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Explains OT systems often run 24/7 continuous processes - "no one working" doesn't mean safe
- Reboots can cause unsafe process states (valves stuck, temperatures uncontrolled)
- OT patches require vendor certification before deployment
- Proposes coordinated maintenance windows with operations team
- Recommends testing patches in staging environment first
- Suggests compensating controls for systems that can't be patched
- Emphasizes safety and availability over immediate patching
- Would document risk acceptance for delayed patching with business justification

</details>

## Mid-Level

### Q1. You've been asked to create an asset inventory for OT security. The plant has been running for 20 years with minimal documentation. You have passive network monitoring deployed but it's only showing about 60% of what operations says exists. How do you approach building a complete OT asset inventory without disrupting operations?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Passive monitoring is foundation but won't see devices that communicate rarely
- Cross-reference with existing documentation - maintenance records, network diagrams
- Physical walkdowns with operations to identify devices on panels
- Examine switch port mappings and MAC address tables
- Serial-connected devices won't appear on network monitoring - need other methods
- Interview operators and engineers about what they interact with
- Use configuration backups to identify PLCs and their I/O
- Historian tag databases may reveal connected devices
- Active scanning is risky in OT but some tools designed for it (use carefully)
- Asset inventory is ongoing, not one-time - new devices added, old removed
- Categories needed: IP vs. serial, controllers vs. HMI vs. network, criticality
- Don't assume accuracy of existing drawings - verify in field

</details>

## Senior / Advanced

### Q1. Your company wants to conduct a cyber risk assessment of the OT environment. The IT security team offers to use their standard risk assessment methodology based on asset value and threat likelihood. The OT team is skeptical that "IT risk methods" apply to operational technology. How do you adapt risk assessment for OT environments, and what factors should be considered that might differ from IT?

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- IT risk focuses on CIA (confidentiality, integrity, availability) - OT adds safety
- Safety consequences (injury, environmental damage) must be factored in
- Physical process understanding required - what happens if this system fails?
- Availability is usually highest priority in OT (opposite of many IT scenarios)
- Asset value in OT isn't just replacement cost - includes production impact
- Threat modeling should include physical consequences, not just data impact
- Existing safety studies (HAZOP, PHA) are input to cyber risk assessment
- IEC 62443 has risk assessment methodology designed for industrial environments
- Consequence-driven approach - work backward from worst outcomes
- Involve process engineers in risk assessment, not just security and IT
- Recovery time is critical - can't just restore from backup in OT
- Consider attack paths that cross IT-OT boundary

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
