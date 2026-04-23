# Privacy Engineering: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. Your company encrypts all customer data and has passed a SOC 2 security audit. A customer asks: "Is my data private?" Marketing wants to say yes. Legal is hesitant. Why might legal be right to hesitate, and what would you need to verify before answering?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Security (encryption, access controls) doesn't automatically mean privacy
- Privacy question is: How is the data being used, not just protected
- Need to verify: Are we collecting more than necessary? Sharing with third parties?
- Need to verify: Can customer access, correct, delete their data?
- Need to verify: Are we using data only for stated purposes?
- A company could be secure but still misuse data in authorized ways
- Legal is right - security audit doesn't answer the privacy question

</details>

## Mid-Level

### Q1. Your marketing team uses a data management platform (DMP) that creates audience segments by combining your first-party customer data with third-party data purchased from data brokers. They use these enriched profiles to target ads across the internet. The CMO asks: "Is this still okay after all the privacy changes?" Walk through the privacy issues in this adtech setup.

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Third-party data enrichment is under increasing regulatory and technical pressure
- Questions about consent and lawful basis for combining first and third-party data
- Third-party cookies are being deprecated - technical foundation changing
- Were customers informed their data would be enriched and used this way?
- Data broker data often has questionable provenance and consent
- Cross-site tracking raises legitimate interests vs. consent questions
- GDPR requires transparency about third-party data sources
- California CPRA gives opt-out of sharing/cross-context behavioral advertising
- Consider transition to first-party data strategy and privacy-safe alternatives
- Contextual advertising as alternative that doesn't require tracking
- Yes, this is "still okay" in some sense, but risk profile is increasing

</details>

## Senior / Advanced

### Q1. Your company is part of a data clean room arrangement with a retail partner. You provide hashed email addresses of your customers, they provide purchase data, and the clean room matches to measure ad campaign effectiveness without either party seeing the other's raw data. The DPO asks you to assess whether this arrangement is privacy-compliant. What questions do you ask?

*Difficulty: ⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Clean rooms reduce data exposure but don't eliminate privacy concerns
- Hashed emails can still be re-identified - hashing isn't anonymization
- Both parties are processing personal data - need lawful basis
- What did customers consent to? Does it cover this kind of matching?
- Questions about clean room operator - are they a processor? Controller?
- What happens to match results? Can they be re-linked to individuals?
- Purpose limitation - is campaign measurement what data was collected for?
- Minimum necessary - what aggregation level is sufficient for the use case?
- Security of the clean room environment and access controls
- Retention of match results and deletion procedures
- Clean rooms are privacy-enhancing but not privacy-proof

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
