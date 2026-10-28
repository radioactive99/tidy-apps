# Groups for Jira

Groups for Jira lets you mention a group in Jira Cloud, add a group as watchers, see who is in a group, and find where a group is used. It runs entirely on Atlassian's platform.

- [Privacy policy](privacy) · [Terms](terms) · [Security](security)
- Support: akshatsodha99@gmail.com

## Mention a group in a comment

Type `@@` followed by the group name in any issue comment:

- `@@dev-team`
- `@@"Platform Team"` (use quotes when the name has spaces)

Every member of the group gets an email from Jira with your comment and a link to the issue. If you edit the comment and add another group, only the new group is emailed.

Nobody is emailed when:
- the comment is restricted to a role or group, because the email would show the comment to people who can't see it
- the group is blocked, isn't on the allow list, or is larger than the size limit (see [Settings](#settings))
- the group doesn't exist

## Notify a group from an issue

1. Open the issue and click **•••** → **Notify a group**.
2. Pick up to 10 groups and write a message.
3. Click **Notify**. The modal shows which groups were notified and which were skipped, with the reason.

## Add a group as watchers

1. Open the issue and click **•••** → **Add group as watchers**.
2. Pick a group and click **Add as watchers**.

Each member is added as a watcher. Large groups are added in the background with a progress bar, and you can close the modal while it runs. Anyone Jira won't add, such as a member who can't see the issue, is counted as failed.

## Group directory

Go to **Apps** → **Group directory**, pick a group, and see its members. Any Jira user can use it, but only for the groups an admin has made visible. Until an admin adds groups in Settings, the directory is empty.

## Group usage report (admins)

Before renaming or deleting a group, check where it is used.

1. Go to **Jira settings** → **Apps** → **Group usage report**.
2. Pick a group and click **Scan**.

The scan checks:
- permission schemes
- notification schemes
- issue security levels
- project roles in every project
- filters and dashboards shared with or editable by the group

The report lists each place, and you can copy it as CSV. Workflows, custom fields and global permissions are not checked yet.

## Settings

Go to **Jira settings** → **Apps** → **Groups for Jira – Settings**. Only Jira administrators can open it.

| Setting | Default | What it does |
|---|---|---|
| Notify groups mentioned in comments | On | Turns `@@` mentions on or off |
| Mention prefix | `@@` | The characters that start a group mention |
| Largest group that can be notified | 50 | Larger groups can't be notified or added as watchers |
| Only these groups can be notified | Empty (all groups) | An allow list |
| Never notify these groups | Empty | A block list that always wins |
| Who can browse group members | Only the groups listed | Which groups the directory shows |

## Emails aren't arriving

Groups for Jira asks Jira to send the email, so Jira's own mail settings apply. If your site has outgoing mail turned off, nobody is emailed. A Jira admin can turn it on under **System** → **Outgoing mail**.
