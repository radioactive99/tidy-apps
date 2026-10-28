# Tree Tidy for Confluence: Privacy Policy

**Effective date:** 28 October 2026
**Provider:** Tidy Apps, operated by Akshat Sodha ("we", "us")
**Contact:** akshatsodha99@gmail.com

## 1. Summary

Tree Tidy for Confluence runs entirely on Atlassian Forge and is eligible for **Runs on Atlassian**:

- The app has no servers of its own. Its code runs, and its data is stored, inside Atlassian's cloud.
- No data is sent outside Atlassian.
- We use no analytics, tracking, cookies or third-party services.
- We have no tool that lets us read your Confluence data or the data the app stores.

## 2. Data the app reads

The app reads the following from your Confluence site through Atlassian's APIs, at the moment a feature is used. It does not keep a copy beyond what section 3 lists.

| Data | Why |
|---|---|
| Space key, ID and home page | To show the tree for the space you are in |
| Page IDs, titles, parent pages and position in the tree | To show the tree, sort it, and preview and undo moves |
| Creation and last-edit order of child pages | To sort by date |
| Whether you can edit a page | To let only editors turn on automatic sorting |
| Pages and blog posts you watch, with their space name and last-edit date | To show **My watches** |
| Page events (page created, updated or moved) | To re-sort parents that have automatic sorting turned on |

## 3. Data the app stores

Stored data lives in Atlassian's Forge hosted storage for your site and is managed by Atlassian. Every stored record except sort rules deletes itself automatically.

| Record | Contents | Kept for |
|---|---|---|
| Sort rules | Space ID, parent page ID and the chosen order | Until someone turns the rule off, the app finds the parent page deleted, or the app is uninstalled |
| Undo history | Space ID, the IDs of the pages a sort or move changed, their previous parent page IDs and the previous order of child page IDs, and the time | 90 days, and only the latest 20 changes per space. An entry is removed as soon as it is undone. |
| Sort timer | Parent page ID and a time, used to group several page changes into one sort | Deleted when the sort runs, and in any case within 1 day |
| Tasks in progress (sort, move, undo, unwatch) | Space ID, the account ID of the person who started the task, progress counts, and short error reasons | 7 days after the task's last update |
| Task step list | Page or content IDs and parent page IDs to process | Deleted when the task ends, and in any case within 7 days |
| Audit trail | Action, space ID, number of pages, sort order, and the account ID of the person who acted | 7 days for entries that name a person; 90 days for the rest |

Account IDs are always erased within 7 days. The app never stores page titles, page content, email addresses or passwords.

## 4. Logs

The app writes technical logs to Atlassian's developer tools, which we can view. Logs contain only counts, outcome codes and HTTP status codes. They never contain page titles, space keys, page IDs or account IDs.

## 5. Who processes the data

**Atlassian** hosts and runs the app as part of your Atlassian cloud subscription. We use no other subprocessors.

## 6. Your rights

All data stays in your Atlassian site, and personal data erases itself within 7 days. Because we have no access to your site's data, requests to access, correct or delete personal data go to your organization's Confluence administrator. Uninstalling the app removes its stored data under Atlassian's data retention policy for Forge apps.

For questions about this policy, contact akshatsodha99@gmail.com.

## 7. Changes

If we change this policy, we will update the effective date above. We will announce material changes in the app's Marketplace release notes.
