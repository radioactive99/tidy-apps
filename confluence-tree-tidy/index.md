# Tree Tidy for Confluence

Tree Tidy for Confluence keeps Confluence Cloud page trees in order. Sort child pages once or keep them sorted, move many pages at once with undo, and stop watching pages in bulk. It runs entirely on Atlassian's platform.

- [Privacy policy](privacy) · [Terms](terms) · [Security](security)
- Support: akshatsodha99@gmail.com

## Open the tree

- **Whole space:** in the space sidebar, click **Tree Tidy**. The tree starts at the space's home page.
- **One page:** on a page, click **•••** → **Sort or move child pages**. The tree starts at that page.

Click **▸** next to a page to open its child pages.

## Sort child pages

1. Open a page in the tree and click **Sort children**.
2. Pick an order:
   - **Title A–Z** or **Title Z–A**. Numbers sort naturally ("Page 2" comes before "Page 10"), and case and accents are ignored.
   - **Oldest first** (by creation date)
   - **Recently edited first**
3. Check the preview. It shows how many pages will move and the new order.
4. Click **Sort**.

The app moves as few pages as possible. Folders, whiteboards and databases stay where they are, and pages are sorted between them.

## Keep a page's children sorted

In the sort window, tick **Keep sorted** before you click **Sort** (or **Save**). From then on, when a page is created, renamed or moved under that parent, the app re-sorts the parent about 30 seconds later. Several changes close together cause a single sort.

Only someone who can edit the parent page can turn this on. To turn it off, open **Sort children** again, untick **Keep sorted**, and click **Save**.

## Move many pages at once

1. Tick the pages you want to move. Pages can come from different parts of the tree.
2. Click **Move selected…** and search for the new parent page in the same space.
3. Check the preview, then click **Move**.

The pages move with their child pages, and land at the end of the new parent in the order the tree showed them. Pages already under the new parent, or that you can't see, are skipped. You can move up to 200 pages at a time.

## Undo

**Undo last sort** or **Undo last move** puts the pages back where they were: under the same parent and in the same order. Pages added since then stay, at the end. Each space keeps its last 20 changes for 90 days, and **Undo** reverses the newest one.

## Keep the page open while it works

Sorting, moving, undoing and unwatching run with your Confluence permissions, step by step, while the app is open. If you close it part-way, the rest doesn't happen. You can run the action again, or undo it.

Refresh the page to see the new order in the Confluence sidebar.

## My watches

Go to **Apps** → **My watches**. It lists the pages and blog posts you watch (the newest 1,000), with their space and when they were last edited.

1. Filter by space, or show only pages that haven't been edited for 30 days, 90 days or a year.
2. Tick pages, or tick **Select all shown**.
3. Click **Unwatch** and confirm.

This only changes your own watches. To watch a page again, open it and click **Watch**.

## What the app doesn't do

- Move pages to a different space.
- Delete drafts. Confluence has no API that lets an app list your drafts.
- Sort the top level of a space (pages next to the home page).
