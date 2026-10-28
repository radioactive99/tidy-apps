# Sprint Fields for Jira

Sprint Fields for Jira puts sprint dates on every issue as real fields you can search, sort and show as columns, and records which issues were added to or removed from a sprint after it started. It runs entirely on Atlassian's platform.

- [Privacy policy](privacy) · [Terms](terms) · [Security](security)
- Support: akshatsodha99@gmail.com

## Set up (admins, 2 minutes)

1. Install the app. Four fields are created: **Sprint Start Date**, **Sprint End Date**, **Sprint Completed Date** and **Sprint Count**.
2. Go to **Jira settings** → **Apps** → **Sprint Fields – Backfill** and click **Run backfill**. This fills the fields and scope history for issues that are already in sprints. After that, the app keeps everything up to date by itself.
3. Optional: add the fields to your screens so they show on the issue view. You don't need to do this to search or sort with them.

## The fields

| Field | Value |
|---|---|
| Sprint Start Date | Start date of the issue's current sprint |
| Sprint End Date | Planned end date of the issue's current sprint |
| Sprint Completed Date | When the issue's last sprint was completed. Empty while the issue is in an open sprint |
| Sprint Count | How many sprints the issue has been in. A count of 3 or more usually means carry-over |

The current sprint is the issue's active or future sprint. If it has none, the fields show its most recent closed sprint. Fields update when a sprint starts, closes or changes dates, and when an issue is moved between sprints.

The fields are read-only. Nobody can edit them by hand.

## Search with JQL

```
"Sprint End Date" <= endOfWeek() AND statusCategory != Done
"Sprint Start Date" >= startOfMonth()
"Sprint Count" >= 3
sprintAddedAfterStart = "1234"
sprintRemovedAfterStart = "1234"
```

Replace `1234` with the sprint's ID. You can find it in the URL of the board or sprint report, or by searching `sprint = "Sprint name"` and opening the Sprint field.

An issue counts as **added after start** if it joined the sprint more than 60 seconds after the sprint started. The 60 seconds cover the issues Jira moves in as the sprint starts. It counts as **removed after start** if it left the sprint while the sprint was active.

## Sprint scope report

Open a project and go to **Apps** → **Sprint scope changes** in the sidebar. Pick a sprint to see three lists, each with issue and story point totals:

- **Committed at start**: issues in the sprint when it started
- **Added after start**
- **Removed after start**

An issue committed at the start and later removed appears in both the committed and removed lists, as in Jira's own sprint report. The report shows up to 1,000 issues and the 50 most recent sprints of the project's boards.

## Limits

- The backfill covers up to 20,000 issues that are currently in a sprint, most recently updated first. Issues that were removed from every sprint before you installed the app have no scope history.
- Story points come from the *Story point estimate* field, or a field named *Story Points*.
- Kanban boards have no sprints and don't appear in the report.
