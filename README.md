# claude-aws-penetration-testing-skill

A Claude Code skill for planning and conducting authorized security assessments of AWS environments, with emphasis on defensive validation and evidence-based reporting.

## Overview

This skill supports cloud security reviews across identity, storage, compute, serverless, networking, and data services. It helps define assessment scope, inspect configurations, identify risky permissions, validate security controls, and produce actionable findings.

Use it only for AWS accounts and resources that the user owns or is explicitly authorized to assess.

## Assessment Areas

- IAM users, roles, policies, and trust relationships.
- S3 bucket access and data exposure controls.
- EC2 instance configuration and metadata protections.
- Lambda permissions, environment configuration, and execution roles.
- Secrets storage and access patterns.
- Container and serverless security posture.
- Network boundaries and security groups.
- Logging, monitoring, and audit coverage.
- Evidence collection and remediation planning.

## Prerequisites

The assessment environment may require:

- AWS CLI.
- Authorized AWS credentials.
- Python 3 and relevant libraries.
- A clearly documented scope and permission boundary.
- A test account or approved assessment window.

Do not use credentials outside the authorized scope.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-aws-penetration-testing-skill.git ~/.claude/skills/aws-penetration-testing
```

## Usage

Invoke the skill for an authorized AWS security assessment:

```text
/aws-penetration-testing
```

Specify the account, regions, resource types, assessment window, allowed techniques, prohibited actions, and emergency contact or stop conditions.

## Recommended Assessment Workflow

1. Confirm written authorization and scope.
2. Identify the AWS accounts and regions in scope.
3. Establish allowed and prohibited testing actions.
4. Begin with non-destructive configuration review.
5. Inspect identity, network, storage, compute, and logging controls.
6. Validate suspected issues using the least invasive method.
7. Collect evidence without exposing secrets or unnecessary data.
8. Assess impact and likelihood.
9. Provide remediation steps and verification guidance.
10. Confirm cleanup and close the assessment.

## Reporting Structure

| Field | Description |
|---|---|
| Finding | Concise security issue |
| Asset | Affected AWS resource |
| Evidence | Reproducible, sanitized proof |
| Impact | Realistic consequence |
| Severity | Risk-based priority |
| Recommendation | Specific remediation |
| Validation | How to confirm the fix |

## Safety Boundaries

- Test only systems within explicit authorization.
- Do not access or extract unrelated customer data.
- Avoid persistence, destructive actions, and service disruption.
- Do not bypass scope restrictions.
- Stop when unexpected sensitive data or production impact is encountered.
- Sanitize evidence and protect credentials.
- Prefer configuration review and safe validation over intrusive techniques.

## Reference Guide

The repository includes `references/advanced-aws-pentesting.md` with additional assessment guidance for identity, serverless, secrets, containers, data services, networking, evidence handling, and stop conditions.

## Repository Contents

- `SKILL.md`: Main assessment workflow and boundaries.
- `references/advanced-aws-pentesting.md`: Advanced authorized assessment guidance.
- `README.md`: Scope, workflow, and reporting guidance.

## Important Note

This skill is not permission to test an AWS environment. Authorization, scope, and platform rules must be confirmed before any active security testing begins.
