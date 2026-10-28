# Groups for Jira: Security

**Security contact:** akshatsodha99@gmail.com

## Reporting a vulnerability

Email akshatsodha99@gmail.com with:
- a description of the issue
- the steps to reproduce it
- the Jira site it affects, if there is one

Please don't test on Jira sites you don't own, and don't share the issue publicly until it's fixed.

We confirm receipt within 2 business days. We fix issues within the timeframes of [Atlassian's Security Bug Fix Policy for Marketplace apps](https://developer.atlassian.com/platform/marketplace/security-bugfix-policy/), and we report incidents to Atlassian as its Marketplace rules require.

## Supported versions

Only the latest version is supported. Atlassian installs new minor versions on every site automatically, so fixes reach every site without any action from you.

## How the app is built

- **Runs on Atlassian.** The app runs on Atlassian Forge with no servers of its own and no external network calls. All data stays in Atlassian's cloud.
- **Permission checks on every request.** Every server function checks permissions before acting:
  - Admin pages require the Jira administrator permission.
  - Issue actions only work on the issue they were opened from, and only if the user can view it.
  - Adding watchers requires the *Manage watchers* permission.
  - Users can only see the progress of jobs they started.
- **Visibility respected.** Comments restricted to a role or group are never emailed. The group directory only shows groups an admin has chosen, and never shows email addresses.
- **Input validated.** All input from the browser is type- and length-checked on the server. Email content is HTML-escaped, and CSV exports neutralise spreadsheet formulas.
- **No sensitive data in errors or logs.** Users see plain error messages, never raw API errors. Logs hold only counts, job IDs and status codes.
- **Data minimisation.** Account IDs are erased within 7 days, and every stored record except settings expires automatically. Details are in the [privacy policy](privacy.md).
- **No credentials.** The app never asks for, stores or handles passwords or API tokens.
- **Dependencies.** Releases are blocked while any known high or critical vulnerability exists in production dependencies. The app runs on a supported Node.js runtime.

## Permissions the app requests

| Scope | Why |
|---|---|
| `read:jira-work` | Read issues, comments, schemes, filters and dashboards |
| `write:jira-work` | Send issue notifications and add watchers |
| `read:jira-user` | Find groups and list their members |
| `manage:jira-configuration` | Read permission, notification and issue security schemes for the usage report |
| `storage:app` | Keep settings, job progress and usage reports |
