# Customer & Org Manager for Jira Service Management: Privacy Policy

**Effective date:** 28 October 2026
**Provider:** Tidy Apps, operated by Akshat Sodha ("we", "us")
**Contact:** akshatsodha99@gmail.com

## 1. Summary

Customer & Org Manager for Jira Service Management runs entirely on Atlassian Forge and is eligible for **Runs on Atlassian**:

- The app has no servers of its own. Its code runs, and its data is stored, inside Atlassian's cloud.
- No data is sent outside Atlassian.
- We use no analytics, tracking, cookies or third-party services.
- We have no tool that lets us read your Jira data or the data the app stores.

## 2. Data the app reads

The app reads the following from your Jira site through Atlassian's APIs, at the moment a feature is used. It does not keep a copy beyond what section 3 lists.

| Data | Why |
|---|---|
| Service projects (ID, key, name) | To let Jira admins choose a project |
| A project's customers: account ID, display name, email address (unless hidden by the customer's privacy settings) and active status | To show the customer list and build CSV exports. This is sent to the browser of the admin using the page and is not stored. |
| Organizations (ID, name) and their members' account IDs | To show which organizations each customer belongs to, and to match organization names during an import |
| Accounts matching an imported email | To reuse an existing account instead of creating a duplicate |
| Your permissions (Jira admin, or admin of the project) | To check you are allowed to use the app |

## 3. Data the app stores

Stored data lives in Atlassian's Forge hosted storage for your site and is managed by Atlassian. Every stored record deletes itself automatically.

| Record | Contents | Kept for |
|---|---|---|
| Background jobs (imports and removals) | Project ID, the account ID of the person who started the job, progress counts, and failures listed by CSV row number or organization name with the reason | 7 days after the job's last update |
| Job work list | For an import: the valid rows of the CSV (emails, display names, organization names). For a removal: the customers' account IDs | Deleted when the job ends, and in any case within 7 days |
| Import organization list | Organization names and IDs used by one import | 7 days |
| Audit trail | Action (import or removal), project ID, number of rows or customers, and the account ID of the person who acted | 7 days |

Customer lists and CSV exports are never stored. Email addresses are stored only in an import's work list while that import runs. The app never stores passwords.

## 4. Logs

The app writes technical logs to Atlassian's developer tools, which we can view. Logs contain only counts, job IDs, job types and HTTP status codes. They never contain names, email addresses, account IDs or organization names.

## 5. Who processes the data

**Atlassian** hosts and runs the app as part of your Atlassian cloud subscription. We use no other subprocessors.

## 6. Your rights

All data stays in your Atlassian site, and everything the app stores erases itself within 7 days. Because we have no access to your site's data, requests to access, correct or delete personal data go to your organization's Jira administrator. Uninstalling the app removes its stored data under Atlassian's data retention policy for Forge apps.

For questions about this policy, contact akshatsodha99@gmail.com.

## 7. Changes

If we change this policy, we will update the effective date above. We will announce material changes in the app's Marketplace release notes.
