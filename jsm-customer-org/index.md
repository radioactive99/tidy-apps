# Customer & Org Manager for Jira Service Management

See, export, import and clean up the customers and organizations of a Jira Service Management project. It runs entirely on Atlassian's platform.

- [Privacy policy](privacy) · [Terms](terms) · [Security](security)
- Support: akshatsodha99@gmail.com

## Where to find it

- **In a service project:** Project settings → **Customers & organizations**. Project admins can use it for their own project.
- **For every project:** Jira settings → Apps → **Customer & Org Manager**. Jira admins pick any service project from a list.

## See and filter customers

The **Customers** tab lists every customer of the project with their name, email, the project's organizations they belong to, and whether their account is active. Filter by name or email, by organization (or *No organization*), and by status.

Emails hidden by a customer's privacy settings show as "hidden". Large projects load in batches, and the counter shows progress.

## Export to CSV

Filter the list, then select **Export N as CSV**. Select all the text in the box, copy it, and paste it into a `.csv` file or a spreadsheet. The columns are `displayName`, `email`, `accountId`, `active` and `organization`. You can import the same file into another project.

Nothing is saved: the CSV is built in your browser each time.

## Import from CSV

1. Open the **Import CSV** tab.
2. Choose a CSV file, or paste the CSV into the box. Columns:
   - `email` (required)
   - `displayName` (optional; the email is used when it's empty)
   - `organization` (optional; several names separated by `;`)
3. Select **Preview**. Nothing changes yet. The preview shows how many customers will be added, which organizations will be created, which existing organizations will be linked to the project, and which rows have problems (invalid or repeated emails, or an organization name shared by two organizations).
4. Select **Import N rows**. The import runs in the background with a progress bar.

For each row, the app creates the customer, or reuses the existing account with that email. A customer with organizations is added to them, and each organization is linked to the project. A customer without organizations is added to the project directly. Rows with problems are skipped.

Up to 1,000 rows per run. Split larger files.

If a row fails, the result lists it by row number with the reason. One known case: when an account with that email already exists but its owner hides their email, the app can't find the account. Add that person by hand.

## Remove customers from the project

1. On the **Customers** tab, filter the list down to the customers you want to remove. To remove one person, search for them.
2. Select **Remove N from project…**. The preview is exactly the customers in the table, and says how many of them also have access through an organization.
3. Tick **I understand** and select **Remove**.

Removed customers lose access to this project's portal. Their accounts, requests and other projects are not touched. Customers who belong to an organization linked to the project keep access through it until you remove them from that organization.

Jira only allows removing customers when the project restricts who can raise requests. On a project open to anyone, each removal fails with that reason.

Up to 2,000 customers per run. Every removal is recorded in the app's audit trail.

## Who can use it

- Project settings page: admins of that project.
- Jira settings page: Jira administrators.
- Only the person who started an import or removal can see its progress.

## Not included yet

- Deactivating portal-only customer accounts
- Filtering by last request date
- XLSX export, and one export covering all projects
