# Awesome Cybersecurity Interview Questions

> Cybersecurity interview questions across specialized domains, with methodology-focused answer guidance.

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Domains](https://img.shields.io/badge/domains-18-green)](./questions/)
[![MyKareer](https://img.shields.io/badge/practice-MyKareer-orange)](https://mykareer.com)

Built and maintained by [VisionSecurityLabs](https://github.com/VisionSecurityLabs), the team behind [MyKareer](https://mykareer.com), a cybersecurity interview practice platform.

---

## What Makes This Different

Most interview question lists test **memorization**. These questions test **methodology**: how you think, prioritize, and respond under pressure. Every question includes:

- The question itself (technical, scenario, hands-on, or behavioral)
- Key points that a strong answer should cover
- Difficulty rating (1-5)

These questions are curated by the team behind [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and progress tracking.

---

## Question Bank

This repo contains a curated selection of questions. The full question bank, including additional questions and interactive evaluation, is available on [MyKareer](https://mykareer.com).

| Domain |
|---|
| [🔍 SOC Analyst](./questions/soc.md) |
| [🚨 Incident Response / DFIR](./questions/incident-response.md) |
| [⚔️ Penetration Testing](./questions/pentest.md) |
| [🦠 Malware Analysis](./questions/malware-analysis.md) |
| [📋 GRC / Compliance](./questions/grc.md) |
| [🛡️ Security Engineer](./questions/security-engineer.md) |
| [🔐 Application Security](./questions/appsec.md) |
| [☁️ Cloud Security](./questions/cloud.md) |
| [🌐 Network Security](./questions/network-security.md) |
| [🔑 Identity & Access Management](./questions/iam.md) |
| [🕵️ Threat Intelligence](./questions/threat-intel.md) |
| [📱 Mobile Security](./questions/mobile-security.md) |
| [🏭 OT / ICS Security](./questions/ot-ics.md) |
| [📡 IoT Security](./questions/iot-security.md) |
| [🟣 Purple Team](./questions/purple-team.md) |
| [🔒 Privacy Engineering](./questions/privacy.md) |
| [🧠 Behavioral](./questions/behavioral.md) |
| [🔐 Cryptography](./questions/crypto.md) |

---

## Question Design Philosophy

These questions are designed to reveal **how candidates think**, not what they memorized.

| Anti-Pattern (Avoid) | Better Approach (Used Here) |
|---|---|
| "What is defense in depth?" | "How would you apply defense in depth to a web app?" |
| "List the IR phases" | "Walk me through your first 30 minutes after discovering a breach" |
| "What port is LDAP?" | "You see LDAP traffic to an external IP. How do you investigate?" |
| "Which encryption is most secure?" | "How do you choose encryption for data at rest vs in transit?" |

**Key points** capture methodology indicators, not keyword matches:

```
# Bad key_point (tests memorization)
- "Uses Wireshark"

# Good key_point (tests methodology)
- "Establishes baseline before investigating anomaly"
- "Considers multiple hypotheses before concluding"
- "Prioritizes containment to limit blast radius"
```

---

## Sample Questions

### SOC Analyst — Junior

**Q: Your company's public website was defaced with a political message, but no customer data appears stolen and the site is still accessible. Your manager asks: "Is this a security incident or just vandalism?" How do you explain the security impact?**

What a strong answer covers:
- This IS a security incident — integrity was compromised (website modified)
- Attacker had write access — what else could they have modified? Database? Configs?
- Customer data might have been accessed even if not obviously exfiltrated
- Need to investigate HOW they got access, not just fix the defacement

---

### Penetration Testing — Mid

**Q: You have compromised a workstation in a corporate environment. Describe your approach to lateral movement while minimizing detection.**

What a strong answer covers:
- Enumerate the environment before moving (avoid noisy scanning)
- Use legitimate credentials and built-in tools (living off the land)
- Understand detection capabilities before choosing a technique
- Document each step for the report

---

### Incident Response — Senior

**Q: You are the IR lead and receive a call at 2 AM — a major financial institution suspects they are in the middle of an active ransomware deployment. What are your first 15 minutes?**

What a strong answer covers:
- Activate IR plan and establish command structure immediately
- Contain first — identify and isolate affected systems before investigating
- Preserve evidence before containment actions alter forensic state
- Establish communication channels (legal, executive, external comms)
- Do not shut down systems without forensic imaging first

---

## Practice Interactively

Reading questions is passive. **Practice is active.**

[MyKareer](https://mykareer.com) lets you practice the full question bank with:
- **Silent mode** — flashcard-style self-rating with answer reveal
- **Voice mode** — record your answer, get live evaluation
- **Progress tracking** — see your improvement across domains over time
- **18 specialized domains** — practice exactly the role you're targeting

**[Start practicing at MyKareer →](https://mykareer.com)**

---

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before submitting.

- Questions must test methodology, not memorization
- No definition questions ("What is X?")
- Key points should capture thinking patterns, not keyword lists
- All contributions fall under the CC BY-NC 4.0 license

---

## License

[Creative Commons Attribution-NonCommercial 4.0 International](./LICENSE)

You may use, share, and adapt these questions for **non-commercial purposes** with attribution to [VisionSecurityLabs](https://github.com/VisionSecurityLabs) and [MyKareer](https://mykareer.com). Commercial use is not permitted.

---

*Maintained by [VisionSecurityLabs](https://github.com/VisionSecurityLabs) | [mykareer.com](https://mykareer.com)*
