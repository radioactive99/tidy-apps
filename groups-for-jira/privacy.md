# Groups for Jira: Privacy Policy

**Effective date:** 28 October 2026
**Provider:** Tidy Apps, operated by Akshat Sodha ("we", "us")
**Contact:** akshatsodha99@gmail.com

## 1. Summary

Groups for Jira runs entirely on Atlassian Forge and is eligible for **Runs on Atlassian**:

- The app has no servers of its own. Its code runs, and its data is stored, inside Atlassian's cloud.
- No data is sent outside Atlassian.
- We use no analytics, tracking, cookies or third-party services.
- We have no tool that lets us read your Jira data or the data the app stores.

## 2. Data the app reads

The app reads the following from your Jira site through Atlassian's APIs, at the moment a feature is used. It does not keep a copy beyond what section 3 lists.

| Data | Why |
|---|---|
| Issue key and summary | To write the notification email and link to the issue |
| Comment text | To find group mentions such as `@@dev-team`, and to quote the comment in the email |
| Comment visibility | To refuse to email comments restricted to a role or group |
| Group names, group IDs and group size | To find and check the groups people pick or mention |
| Group members' account IDs, display names and avatars | To add members as watchers and to show the group directory. Any email addresses Jira returns are discarded, never shown or stored. |
| Your permissions (for example, Jira admin or *Manage watchers*) | To check you are allowed to use a feature |
| Jira configuration: permission and notification schemes, issue security levels, project roles, shared filters and dashboards | To build the group usage report |

## 3. Data the app stores

Stored data lives in Atlassian's Forge hosted storage for your site and is managed by Atlassian. Every stored record except settings deletes itself automatically.

| Record | Contents | Kept for |
|---|---|---|
| Settings | Your choices, and the IDs of groups you allow, block or show in the directory | Until the app is uninstalled |
| Mention log | Issue key, comment ID, and the IDs and names of groups notified or skipped for that comment | 180 days, so editing an old comment doesn't email the same group twice |
| Background jobs (adding watchers) | Issue key, group, the account ID of the person who started the job, and progress counts | 7 days after the job's last update |
| Job member list | Account IDs of the group's members, used while adding them as watchers | Deleted when the job ends, and in any case within 7 days |
| Usage report | Names of the schemes, projects, filters and dashboards that use a group | The latest report per group only, for up to 90 days |
| Audit trail | Action, issue key, group names, recipient count, and the account ID of the person who acted, where there is one | 7 days for entries that name a person; 90 days for the rest |

Account IDs are always erased within 7 days. The app never stores email addresses, comment text or passwords.

## 4. Emails

When someone notifies or mentions a group, Jira sends the email through its own notification service, not through us. The email goes only to group members who are allowed to view the issue. It contains the sender's name, the group names, the issue key and summary, a link to the issue, and the message or comment text. Comments restricted to a role or group are never emailed.

## 5. Logs

The app writes technical logs to Atlassian's developer tools, which we can view. Logs contain only counts, job IDs, job types and HTTP status codes. They never contain comment text, names, email addresses, account IDs or issue keys.

## 6. Who processes the data

**Atlassian** hosts and runs the app as part of your Atlassian cloud subscription. We use no other subprocessors.

## 7. Your rights

All data stays in your Atlassian site, and personal data erases itself within 7 days. Because we have no access to your site's data, requests to access, correct or delete personal data go to your organization's Jira administrator. Uninstalling the app removes its stored data under Atlassian's data retention policy for Forge apps.

For questions about this policy, contact akshatsodha99@gmail.com.

## 8. Changes

If we change this policy, we will update the effective date above. We will announce material changes in the app's Marketplace release notes.
