# Tree Tidy for Confluence: Security

**Security contact:** akshatsodha99@gmail.com

## Reporting a vulnerability

Email akshatsodha99@gmail.com with:
- a description of the issue
- the steps to reproduce it
- the Confluence site it affects, if there is one

Please don't test on Confluence sites you don't own, and don't share the issue publicly until it's fixed.

We confirm receipt within 2 business days. We fix issues within the timeframes of [Atlassian's Security Bug Fix Policy for Marketplace apps](https://developer.atlassian.com/platform/marketplace/security-bugfix-policy/), and we report incidents to Atlassian as its Marketplace rules require.

## Supported versions

Only the latest version is supported. Atlassian installs new minor versions on every site automatically, so fixes reach every site without any action from you.

## How the app is built

- **Runs on Atlassian.** The app runs on Atlassian Forge with no servers of its own and no external network calls. All data stays in Atlassian's cloud.
- **Your permissions, not the app's.** Sorting, moving, undoing and unwatching run as the signed-in user, so Confluence only lets people change pages they are allowed to change, and the tree only shows pages they can see.
- **Automatic sorting.** Re-sorting after page changes runs as the app. Only someone who can edit the parent page can turn it on for that page, and it only reorders that page's children.
- **Checks before every bulk change.** Moves and sorts show a preview and need a confirmation. Moves are re-checked on the server when they start: the target must be in the same space, and a page can't be moved under itself.
- **Context, not browser input.** The space comes from where the app is opened, not from the browser. Users can only run and see tasks they started.
- **Input validated.** Page and content IDs from the browser must be plain numeric IDs, and text input is length-checked and escaped in searches.
- **No sensitive data in errors or logs.** Users see plain error messages, never raw API errors. Logs hold only counts and status codes.
- **Data minimisation.** Account IDs are erased within 7 days, and every stored record except sort rules expires automatically. Details are in the [privacy policy](privacy.md).
- **No credentials.** The app never asks for, stores or handles passwords or API tokens.

## Permissions the app requests

| Scope | Why |
|---|---|
| `read:confluence-content.summary` | Receive page created, updated and moved events for automatic sorting |
| `write:confluence-content` | Move pages, and remove your watches |
| `search:confluence` | List the pages you watch, and find a target page for a move |
| `read:page:confluence` | Read page titles, parents and your edit permission |
| `read:hierarchical-content:confluence` | List a page's child pages, folders, whiteboards and databases in tree order |
| `read:content.metadata:confluence` | Read a page's ancestors, to stop a page being moved under itself |
| `read:space:confluence` | Find the space and its home page |
| `storage:app` | Keep sort rules, undo history and task progress |
