# Customer & Org Manager for Jira Service Management: Security

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
  - On a project settings page, the project comes from Jira, not the browser, and the user must be an admin of that project.
  - The Jira settings page requires the Jira administrator permission.
  - Organization members can only be listed for organizations linked to the project.
  - Users can only see or cancel jobs they started.
- **Safe bulk changes.** Imports always show a preview first and are re-checked on the server from the file itself. Removals show exactly who will be removed, need an explicit confirmation, and are recorded in an audit trail.
- **Input validated.** All input from the browser is type- and length-checked on the server. CSV rows are validated (email format, duplicates, row limits), and CSV exports neutralise spreadsheet formulas.
- **No sensitive data in errors or logs.** Users see plain error messages, never raw API errors, which can contain emails. Failures are recorded by row number, not by email. Logs hold only counts, job IDs and status codes.
- **Data minimisation.** Customer lists and exports are never stored. Everything the app stores expires within 7 days. Details are in the [privacy policy](privacy.md).
- **No credentials.** The app never asks for, stores or handles passwords or API tokens.
- **Dependencies.** Releases are blocked while any known high or critical vulnerability exists in production dependencies. The app runs on a supported Node.js runtime.

## Permissions the app requests

| Scope | Why |
|---|---|
| `read:servicedesk-request` | List service projects for the Jira settings page |
| `manage:servicedesk-customer` | List, create and remove customers, and create, link and fill organizations |
| `read:jira-user` | Find the existing account for an imported email |
| `read:jira-work` | Check the user's project and Jira admin permissions |
| `storage:app` | Keep job progress and the audit trail |
