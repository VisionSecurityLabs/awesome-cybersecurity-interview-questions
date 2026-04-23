# IoT Security: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. What are the main attack surfaces of a modern vehicle that a penetration tester should consider?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: technical*

<details>
<summary>What a strong answer covers</summary>

- External wireless: Cellular, Wi-Fi, Bluetooth, TPMS, Key Fob (KES)
- Internal interfaces: Infotainment console, USB, OBD-II connector, CAN bus
- Physical access: Direct CAN bus splicing, ECU tampering
- Remote diagnostics: OnStar-like systems, telematics
- V2V/V2I communication: DSRC protocols
- Long-range vs near-range external inputs

</details>

## Mid-Level

### Q1. You are assessing a connected vehicle's security. A colleague suggests sending fuzzing traffic over the OBD-II port to see how the car responds. Why is this a bad idea, and how would you approach the assessment more carefully?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies safety risk: CAN bus controls brakes, steering, engine management
- Notes that fuzzing can trigger physical actuators in unpredictable ways
- Raises the difference between a lab vehicle and a vehicle with people inside
- Proposes passive monitoring before any active interaction
- Suggests establishing a baseline of known-good traffic first
- Recommends a controlled test environment with the vehicle on a lift
- Defines go/no-go criteria before each test step
- Notes that permission from the OEM and a safety officer may be required

</details>

## Senior / Advanced

### Q1. You have extracted firmware from a target ECU. The binary is 2 MB, unknown architecture, and has no obvious strings. Walk me through how you decide whether to continue and how you make progress without spending weeks blindly.

*Difficulty: ⭐⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Starts with entropy analysis to identify compressed or encrypted regions
- Uses binwalk or similar to detect embedded filesystems or known signatures
- Attempts to identify the architecture from byte patterns, not assumptions
- Checks for a bootloader section which is often less obfuscated
- Searches for cross-references and repeating byte patterns to find code structure
- Sets a time-box decision point: if no progress in X hours, escalates or scopes differently
- Does not claim to reverse the entire binary: identifies the most valuable target areas
- Considers whether the firmware update mechanism is a faster path than static RE

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
