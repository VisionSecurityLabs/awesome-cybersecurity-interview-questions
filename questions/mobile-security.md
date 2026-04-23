# Mobile Security: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. Law enforcement brings you a locked, powered-off iPhone from a suspect. They want "everything on it." Walk through how you think about what is and is not realistic to extract, and what decisions you make first.

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not promise "everything": sets realistic expectations based on device and iOS version
- Asks about iOS version and device model before making any claims about extractability
- Prioritizes preserving the device state: do not power on, do not connect to unknown networks
- Explains the impact of the Secure Enclave and encryption on full disk access
- Discusses what is potentially available: backups, iCloud sync, carrier records vs. on-device data
- Raises chain of custody and legal authorization before touching the device
- Does not conflate "we can image the storage" with "we can read the data"
- Notes that the forensic approach depends heavily on whether law enforcement has a legal order for iCloud data

</details>

## Mid-Level

### Q1. You're assessing a mobile banking app's data storage. You have a rooted Android device and have extracted the app's data directory. Walk through your assessment approach: what files and locations do you examine, and what findings would you flag as critical?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Examines SharedPreferences XML files for plaintext credentials or tokens
- Checks SQLite databases for unencrypted sensitive data (account numbers, transaction history)
- Looks for plaintext API keys or secrets in app data or cache directories
- Examines app's internal storage for session tokens stored insecurely
- Checks if app uses Android Keystore for cryptographic keys vs. file-based storage
- Looks for PII in log files (common developer mistake)
- Critical findings: Any plaintext passwords, auth tokens, or encryption keys
- Critical findings: Unencrypted PII or financial data in databases
- Verifies encryption is actually protecting data vs. just encoding (Base64 isn't encryption)
- Documents findings with evidence and severity ratings

</details>

## Senior / Advanced

### Q1. Your CEO insists on BYOD for all employees including contractors because she does not want to issue corporate phones. You have 90 days to design a program. What decisions do you force the executive team to make, and what do you refuse to compromise on?

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Identifies the decisions that cannot be made by security alone: acceptable use policy, legal jurisdiction for monitoring, data residency
- Raises the contractor question explicitly: personal devices with corporate data and employment ending creates a data recovery problem
- Refuses to compromise on: containerization or MAM to separate corporate data, ability to remote wipe corporate data (not the whole device), minimum OS version requirements
- Proposes a tiered access model: contractors get browser-only access, employees get managed app access
- Addresses the privacy tension: what monitoring is legal and disclosed on a personal device?
- Notes that 90 days is not enough to do everything: defines what "done" means for the initial rollout
- Does not build a program the CEO will reverse in three months: aligns on the non-negotiables upfront

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
