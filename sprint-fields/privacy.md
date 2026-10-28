# Sprint Fields for Jira: Privacy Policy

**Effective date:** 28 October 2026
**Provider:** Tidy Apps, operated by Akshat Sodha ("we", "us")
**Contact:** akshatsodha99@gmail.com

## 1. Summary

Sprint Fields for Jira runs entirely on Atlassian Forge and is eligible for **Runs on Atlassian**:

- The app has no servers of its own. Its code runs, and its data is stored, inside Atlassian's cloud.
- No data is sent outside Atlassian.
- We use no analytics, tracking, cookies or third-party services.
- We have no tool that lets us read your Jira data or the data the app stores.
- The app stores no personal data.

## 2. Data the app reads

The app reads the following from your Jira site through Atlassian's APIs, when a sprint or issue changes, during a backfill, or when someone opens the scope report. It does not keep a copy beyond what sections 3 and 4 list.

| Data | Why |
|---|---|
| An issue's Sprint field and created date | To work out its sprint dates and sprint count |
| An issue's change history | To find when it was added to or removed from each sprint. Other changes in the history, and who made them, are ignored |
| Sprint dates, state and name | To fill the date fields, and to list sprints in the report |
| A project's boards | To list its sprints in the report |
| Issue key, summary, status and story points | To show the scope report. Read with the viewer's own permissions |
| The site's field list | To find the Sprint and story point fields |
| Your permissions | To check you are a Jira administrator before you run a backfill |

## 3. Data the app writes to your Jira issues

These values become part of your Jira issues, like any other field.

| Data | Contents |
|---|---|
| Sprint Start Date, Sprint End Date, Sprint Completed Date, Sprint Count | Dates and a number taken from the issue's sprints |
| Issue property `sprintScope` | IDs of the sprints the issue was committed to, added to after start, and removed from after start |

They stay on the issues until the issue is deleted. After an uninstall the fields are no longer shown; the issue property stays on the issue until an admin removes it through Jira's REST API.

## 4. Data the app stores

Stored data lives in Atlassian's Forge hosted storage for your site and is managed by Atlassian. Every stored record deletes itself automatically.

| Record | Contents | Kept for |
|---|---|---|
| Background jobs (backfill, sprint updates) | Job type, issue count, progress counts and plain error messages. No account IDs, issue keys or names | 90 days after the job's last update |
| Job issue list | Numeric IDs of the issues a job is processing | Deleted when the job ends, and in any case within 7 days |
| Last backfill | The ID of the latest backfill job, so the settings page can show its progress | 90 days |

The app never stores account IDs, email addresses, issue summaries or passwords.

## 5. Logs

The app writes technical logs to Atlassian's developer tools, which we can view. Logs contain only counts, job IDs, event types and HTTP status codes. They never contain names, account IDs, issue keys or issue content.

## 6. Who processes the data

**Atlassian** hosts and runs the app as part of your Atlassian cloud subscription. We use no other subprocessors.

## 7. Your rights

All data stays in your Atlassian site, and the app keeps no personal data. Because we have no access to your site's data, requests about your data go to your organization's Jira administrator. Uninstalling the app removes its stored data under Atlassian's data retention policy for Forge apps.

For questions about this policy, contact akshatsodha99@gmail.com.

## 8. Changes

If we change this policy, we will update the effective date above. We will announce material changes in the app's Marketplace release notes.
