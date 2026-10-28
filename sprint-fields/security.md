# Sprint Fields for Jira: Security

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
- **Permission checks on every request.**
  - The backfill page requires the Jira administrator permission.
  - The scope report searches with the viewer's own permissions, so it only lists issues they can already see.
- **Read-only fields.** The four sprint fields can only be written by the app, never by users or other apps.
- **Input validated.** Sprint IDs from the browser are checked to be positive whole numbers before they reach a query.
- **No sensitive data in errors or logs.** Users see plain error messages, never raw API errors. Logs hold only counts, job IDs and status codes.
- **Data minimisation.** The app stores no account IDs or issue content, and every stored record expires automatically. Details are in the [privacy policy](privacy.md).
- **No credentials.** The app never asks for, stores or handles passwords or API tokens.
- **Dependencies.** Releases are blocked while any known high or critical vulnerability exists in production dependencies. The app runs on a supported Node.js runtime.

## Permissions the app requests

| Scope | Why |
|---|---|
| `read:jira-work` | Read issues, their change history and the field list; receive sprint and issue events |
| `write:jira-work` | Save the `sprintScope` issue property |
| `read:sprint:jira-software` | Read sprint dates and list a board's sprints |
| `read:board-scope:jira-software` | List a project's boards for the scope report |
| `read:project:jira` | Required by Jira alongside board access |
| `write:app-data:jira` | Write the app's own custom field values |
| `storage:app` | Keep background job progress |
