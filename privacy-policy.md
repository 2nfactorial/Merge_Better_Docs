# Privacy Policy

**Company:** 2nfactorial
**App:** MergeBetter – Jira Merge Policies
**Effective Date:** March 17, 2026
**Contact:** 2nfactorial@gmail.com

---

## 1. Introduction

2nfactorial ("we", "us", "our") operates the MergeBetter app ("the App"), available on the Atlassian Marketplace. This Privacy Policy explains what data the App collects, how it is used, and your rights regarding that data.

By installing or using the App, you agree to the practices described in this policy.

---

## 2. What Data We Collect

### 2.1 Data You Provide
When configuring the App, administrators create **Merge Policies** consisting of:
- Policy name and optional description
- Branch pattern rules (e.g. `main`, `release-*`)
- JQL queries used to validate Jira issues
- Rejection messages shown to developers

This data is entered manually by Jira administrators and stored within the App.

### 2.2 Data Processed at Runtime
When a GitHub Actions workflow calls the App's webhook, the following data is submitted and processed:
- **Jira issue key** (e.g. `ABC-123`) — extracted from the PR title
- **Branch name** (e.g. `main`) — the PR's target branch
- **Policy ID** (optional) — to target a specific policy

This data is used solely to evaluate whether a pull request meets the configured merge policy. It is **not stored** after the request is processed.

### 2.3 Data Accessed from Jira
The App reads Jira issue data via the Atlassian Forge platform using the `read:jira-work` scope. This includes:
- Issue status, fix version, issue type, and other fields referenced in your JQL queries

This data is accessed in real-time per request and is **never stored or transmitted** outside of Atlassian's infrastructure.

---

## 3. What Data We Do NOT Collect

We do **not** collect or store:
- Personal information (names, email addresses, phone numbers)
- Jira user accounts or profile data
- GitHub tokens, credentials, or repository contents
- PR descriptions, code, or commit history
- Browser data, cookies, or analytics
- Payment or billing information

---

## 4. How Data Is Stored

Policy configuration data (rules, JQL, branch patterns) is stored using **Atlassian Forge Key-Value Storage (KVS)**. This storage:
- Is scoped to your specific Jira installation
- Runs entirely within Atlassian's infrastructure
- Is not accessible to 2nfactorial or any third party
- Is automatically deleted if you uninstall the App

---

## 5. How Data Is Shared

We do **not** sell, rent, or share your data with any third parties.

The App communicates only with:
- **Atlassian's Jira REST API** — to validate issue conditions against your JQL queries
- **Atlassian Forge platform** — for storage and execution (managed by Atlassian)

No data is sent to 2nfactorial servers. The App has no external server infrastructure — it runs entirely on Atlassian's Forge platform.

---

## 6. Data Residency

Because the App runs entirely on Atlassian Forge with no external servers, data residency is governed by Atlassian's data residency policies. Please refer to [Atlassian's Data Residency documentation](https://www.atlassian.com/trust/data-residency) for details.

---

## 7. Data Retention

- **Policy configuration data** is retained until you delete it within the App or uninstall the App.
- **Runtime webhook data** (issue key, branch name) is processed in memory only and is not persisted.

---

## 8. Security

The App is built on Atlassian Forge, which provides:
- OAuth 2.0 token-based authentication (no stored passwords or API tokens)
- Encrypted storage via Atlassian KVS
- Sandboxed execution within Atlassian's infrastructure

The webhook URL acts as a shared secret. We recommend storing it as a GitHub Actions secret and rotating it periodically.

---

## 9. Children's Privacy

The App is intended for professional/enterprise use and is not directed at children under the age of 13. We do not knowingly collect data from children.

---

## 10. Changes to This Policy

We may update this Privacy Policy from time to time. When we do, we will update the Effective Date at the top. Continued use of the App after changes constitutes acceptance of the updated policy.

Significant changes will be communicated via the Atlassian Marketplace listing page.

---

## 11. Your Rights (GDPR)

If you are located in the European Economic Area (EEA), you have the right to:
- Access the personal data we hold about you
- Request correction or deletion of your data
- Object to processing of your data
- Request data portability

Since the App stores no personal data beyond what you explicitly enter as policy configuration, and all data is held within Atlassian's infrastructure, most GDPR rights are exercised through your Atlassian account settings.

To make a data request, contact us at: **2nfactorial@gmail.com**

---

## 12. Contact

If you have questions about this Privacy Policy or the App's data practices:

**2nfactorial**
Email: 2nfactorial@gmail.com
Atlassian Marketplace: [MergeBetter listing](#)

---

*This privacy policy was written for the MergeBetter Forge app distributed on the Atlassian Marketplace by 2nfactorial.*
