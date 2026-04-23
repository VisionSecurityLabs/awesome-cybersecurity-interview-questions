# Cloud Security: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. You inherit an AWS account with 200 S3 buckets from an acquired company. How do you assess and prioritize their security risks? What would you check first?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Prioritizes by data sensitivity and public exposure risk
- Checks public access block settings first (biggest risk)
- Reviews bucket policies and ACLs for overly permissive access
- Verifies encryption settings for sensitive data
- Uses tools like AWS Config or S3 inventory for scale

</details>

## Mid-Level

### Q1. A data science team deployed p3.16xlarge GPU instances in ap-southeast-2 for "testing" and generated a $47,000 bill in one weekend. Finance is furious. You need to prevent this from happening again while still allowing legitimate workloads. How would you use AWS Organizations to implement guardrails?

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Proposes SCPs to restrict expensive instance types
- Would limit which regions can be used (deny list for unused regions)
- Understands SCPs restrict, they don't grant permissions
- Creates exception process for legitimate expensive workload requests
- Considers OU structure to apply different policies to different teams
- Implements budget alerts as additional control
- Would work with data science to understand their actual needs
- Balances prevention with enabling legitimate use cases

</details>

## Senior / Advanced

### Q1. Your company just acquired a startup that has been running everything in a single AWS account with 50+ developers having admin access. You need to integrate them into your organization's multi-account structure. The startup's CTO is resistant: "We ship fast because everyone can do everything." How do you approach this integration while addressing their concerns?

*Difficulty: ⭐⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Acknowledges their velocity concern - security shouldn't slow them down
- Proposes workload isolation via separate accounts while maintaining agility
- Explains account boundaries provide blast radius containment
- Designs developer experience with SSO and role switching
- Creates SCPs that block dangerous actions without blocking deployment
- Implements centralized logging without disrupting their workflow
- Plans phased migration to avoid big-bang disruption
- Addresses their specific use cases with targeted permissions

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
