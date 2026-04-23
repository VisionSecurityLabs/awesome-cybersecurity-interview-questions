# Cryptography: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. A developer asks you to choose between bcrypt, Argon2, and PBKDF2 for password hashing in a new application. They want "the most secure one." How do you approach this decision?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not answer "Argon2 always wins" without asking questions first
- Asks about the deployment environment: is memory-hardness a constraint (embedded, shared hosting)?
- Asks about compliance requirements: some standards mandate specific algorithms
- Explains that all three are acceptable for password hashing; the choice is about fit
- Recommends Argon2id as the modern default for most new applications
- Stresses that configuration matters more than algorithm choice: cost factor, memory, parallelism
- Notes that the worst outcome is using a fast hash like SHA-256 or MD5, not choosing "wrong" among these three

</details>

## Mid-Level

### Q1. A service stores AES encryption keys in environment variables, "because that is where all the other secrets go." What is your response, and what options do you walk through with the team?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Does not dismiss env vars as useless: they are better than hardcoded keys in source
- Identifies the real risk: env vars are accessible to any process in the same environment, logged in crash dumps, exposed in container metadata endpoints
- Distinguishes between key storage and secret storage: encryption keys need stricter controls than API tokens
- Introduces the concept of a key management service (KMS) as the appropriate control
- Explains envelope encryption: use KMS to encrypt a data key, store the encrypted key at rest
- Raises key rotation: env vars make rotation operationally painful
- Does not propose a perfect solution that the team will ignore; offers a migration path

</details>

## Senior / Advanced

### Q1. Your organization's security team learned that NIST has finalized the first post-quantum cryptography standards (ML-KEM/Kyber, ML-DSA/Dilithium). The CISO asks: "We have TLS everywhere, PKI for internal services, and signed firmware updates. How do we migrate to post-quantum cryptography, what's the timeline, and what do we do first?" Walk me through your strategic approach.

*Difficulty: ⭐⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Inventory first: Catalog all cryptographic assets (algorithms, key sizes, libraries, HSMs)
- Crypto-agility assessment: Can systems swap algorithms without major rewrites?
- Prioritization: Start with long-lived secrets (TLS certs, code signing, firmware keys)
- Hybrid approach: Combine classical + PQC during transition (e.g., X25519 + Kyber)
- Timeline awareness: Harvest-now-decrypt-later attacks mean urgent data protection needs
- Vendor dependencies: Track when OpenSSL, BoringSSL, AWS, Azure support PQC
- Testing strategy: PQC increases key/signature sizes - test for MTU, bandwidth, storage impacts
- Certificate lifecycle: Plan for CA infrastructure updates and certificate re-issuance

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
