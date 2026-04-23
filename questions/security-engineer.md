# Security Engineer: Interview Questions

> Part of the [awesome-cybersecurity-interview-questions](https://github.com/VisionSecurityLabs/awesome-cybersecurity-interview-questions) collection.
> Practice these questions interactively at [MyKareer](https://mykareer.com).

---

## Table of Contents

- [Junior / Entry-Level](#junior-entry-level)
- [Mid-Level](#mid-level)
- [Senior / Advanced](#senior-advanced)

---

## Junior / Entry-Level

### Q1. A pull request just came through with Terraform code that creates an S3 bucket. Looking at the config, you notice the bucket has no encryption specified and "block_public_access" is set to false. The developer says "it's just for logs, it doesn't matter." How do you evaluate this and what's your response?

*Difficulty: ⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Questions whether "just logs" could contain sensitive data
- Explains risk of public S3 buckets (common breach vector)
- Proposes encryption at rest as low-cost security improvement
- Suggests IaC scanning in CI/CD to catch issues automatically
- Balances security requirements with developer concerns
- Doesn't just block - explains the reasoning
- Considers policy-as-code to prevent this pattern

</details>

## Mid-Level

### Q1. A small team of four engineers needs to deploy a B2B SaaS web application on AWS. They currently run everything on one EC2 instance and want to "do it properly." They cannot afford a dedicated security engineer. Walk me through what you tell them to prioritize, what you explicitly tell them to skip for now, and why.

*Difficulty: ⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Prioritizes highest-impact basics first: IAM least privilege, MFA on the root account, no access keys in code
- Recommends enabling GuardDuty and Security Hub as low-effort continuous monitoring
- Pushes for S3 block public access as a default, not a feature to configure
- Explicitly deprioritizes: WAF, complex VPC design, and custom KMS until they have more scale
- Recommends Terraform or CDK from the start to avoid configuration drift, not manual console work
- Raises that "one EC2 instance" means one blast radius: pushes for at minimum a separate DB instance
- Does not prescribe a reference architecture: asks what the application actually does before designing
- Notes that a security review once a quarter is better than a perfect architecture they cannot operate

</details>

## Senior / Advanced

### Q1. You're building a security platform team to serve 500 developers. What do you build and how?

*Difficulty: ⭐⭐⭐⭐⭐ &nbsp;|&nbsp; Format: scenario*

<details>
<summary>What a strong answer covers</summary>

- Secure templates and golden images
- Self-service security scanning in CI/CD
- Centralized secrets management
- Security guardrails, not gates
- Developer documentation and training
- Security champions program
- Metrics: developer adoption, MTTD/MTTR
- Make secure path the easy path

</details>
---

> **Want more?** This is a sample. The full question bank for this domain is available on [MyKareer](https://mykareer.com), where you can practice interactively with voice mode and live evaluation.

**[Practice the full question bank at MyKareer →](https://mykareer.com)**

---
