# My Finances

A personal monthly finance tracker that runs entirely in your browser — no installs, no account, no internet needed.

## How to use it

Double-click `index.html` and it opens in your browser. That's it.

Your data is saved automatically in that browser on this computer. Stick with the same browser (e.g. always Chrome or always Edge) so your data is always there. Clearing the browser's site data/history will erase it.

**Important — back up your data.** Because the data lives inside one browser on this one computer, it is *not* shared between browsers (Chrome vs. another browser each have their own separate copy), *not* shared between computers, and it would be lost if you reformat. Use the **Backup & Restore** panel at the bottom of the app:

- **Export backup** downloads a small `.json` file with everything in it. Save it somewhere safe — the Google Drive folder next to this app is a good spot. Do this every so often, and after entering a lot of transactions.
- **Import backup** loads a backup file back in — use it to restore after a reformat, or to copy your data into a different browser or a new computer. Importing replaces whatever is currently in that browser (it asks first).

## What it does

The app has four views, switchable with the tabs at the top:

### Income Statement (default)

- **Add transactions** of four types:
  - **Fixed Cost / Spending** — date, business, category, and amount, with the option to split one purchase across multiple categories (e.g. a Costco run split between Groceries and Household).
- **Custom categories** — a set of common categories is built in, but you can add your own under **"Manage categories"** (a collapsible section at the bottom of the Expenses by Category panel), or just type a new one straight into the category box when adding a transaction. Your custom categories are saved and show up as suggestions from then on, and can be removed anytime.
  - **Savings / Investing** — date, account, and amount. **Account** is a fixed list of tags: Savings, 401(k), 403(b), Brokerage, Roth IRA, Traditional IRA, HSA, ESPP. The pre-tax ones (401(k), 403(b), Traditional IRA, HSA) are marked in the dropdown, since those contributions lower your AGI. The amount can be **negative**, which represents pulling money back out of that bucket into your spending pool for the month (it reduces Saved & Invested and increases Left Over).
  - **Reimbursements / refunds** — when someone pays you back (a person covering their share, or a company refund), check **"This is a reimbursement or refund"** on a Fixed Cost or Spending entry. Enter it as a positive amount against the same category as the original expense; it's subtracted from that category (and added back to Left Over) instead of counting as income. Example: a $100 phone bill plus a $30 reimbursement from a roommate makes Expenses by Category show Phone at $70. Use the same type (Fixed Cost / Spending) as the original bill. Reimbursements show a green "reimbursement" tag in the transaction list.
- **Income sources** — enter each source of income for the month (there's a one-click "copy from last month" when a new month starts). Each source carries a **tax-type tag**: **Earned** (job), **Capital Gains** (stock sales), **Dividend**, **Interest** (e.g. high-yield savings), or **Not Taxable** (e.g. VA disability benefits). Pick the tag when adding, or click the tag on any row to cycle it. The Dashboard totals income by tag for the year — handy at tax time.
- **Monthly picture** (shown by default for the current month):
  - Total income, total expenses (fixed costs + spending), amount saved & invested, and money left over — shown as whole dollars (no cents).
  - Left over turns **red** with an "Overspent by …" note if you spent more than you earned. Saved & Invested also turns **red** if you pulled more out of savings/investing that month than you put in (a negative total).
  - **Where Your Income Went** — a pie chart of income by type: fixed costs, spending, savings, investing, and left over. If a savings/investing total is negative that month (money pulled back out), it stays in the legend with its true negative value — a pie can't draw a negative wedge, and a note says so.
  - **Budget-goal check:** the pie legend's percentages are color-coded green/red against target goals — Fixed Costs under 60%, Spending under 10%, Savings at least 5%, Investing at least 25%. Green means you're on target for that goal, red means you're off. All four goals are always shown (even at $0) so you can see what still needs attention.
  - **Expenses by Category** — a horizontal bar chart of fixed costs + spending split by category (largest first). Bars are sized to the dollar amount, each row shows the amount and its % of income, and a total line sits underneath.
- **Filter transactions** — dropdowns above the transaction list narrow it by type (fixed/spending/savings/investing) and by category.
- **Edit transactions** — click the ✎ pencil on any row to load it back into the form, change anything (including splits), and hit "Save Changes". Cancel anytime.

### Balance Sheet

- **Assets** — enter what you own, split into two sections:
  - **Liquid** — cash-like accounts you could tap quickly (checking, savings, brokerage, cash management).
  - **Illiquid** — things that take time to sell (car, home, collectibles).
  - When adding an asset, pick **Liquid** or **Illiquid** from the dropdown. Each section shows its own subtotal, and you can reorder within a section with the ▲ / ▼ buttons.
- **Liabilities** — enter what you owe (credit cards, car loan, student loans, mortgage balance…).
- **Four summary tiles**: Total Assets, Total Liabilities, **Net Worth** (all assets − liabilities), and **Liquid Net Worth** (liquid assets only − *all* liabilities). Net Worth and Liquid Net Worth turn red when negative — it's common for Liquid Net Worth to be negative if you carry a mortgage, since the home isn't counted. Totals are whole dollars; individual line items keep their exact cents.
- The **Net Worth Trend** chart lives on the **Dashboard** view (see below).
- Each month keeps its own asset/liability values — use **"Copy from last month"** at the start of a new month, then **type the new amount right into each row** (the values are editable in place; totals and the trend chart update as you go). A value of **$0 is allowed**, so if a credit card is paid off or an account is emptied that month, just set it to 0 instead of deleting the row.

### Dashboard

A year-at-a-glance view. The header shows just the **year** here, and the ‹ › arrows step a whole year at a time (2026 → 2027…), the same way the other views step between months.

- **Running totals** for every month you've entered in that year: Income, Fixed Costs, Expenses (fixed costs + spending), Saved, and Invested. Reimbursements and savings/investing pull-outs are netted in, so these match what the monthly views show, summed.
- **Income by Type** — the year's income split into Earned / Capital Gains / Dividend / Interest / Not Taxable (with percentages), driven by the tags on your income sources.
- **Savings & Investing by Account** — the year's contributions broken out by account tag, with pre-tax accounts marked. Negative means money pulled back out.
- **Expenses by Category** — the year's fixed costs + spending combined and totaled by category (largest first), the same categories used elsewhere in the app. Reimbursements/refunds are netted in.
- **Estimated AGI** — a rough adjusted-gross-income estimate for the year: taxable income (earned + capital gains + dividends + interest) minus pre-tax contributions (401(k), 403(b), Traditional IRA, HSA). Not-taxable income is excluded. **This is a ballpark for your own tracking, not a filing figure** — real AGI includes adjustments this app doesn't track (self-employment tax, student loan interest, deductions, employer HSA contributions, and more). You can also ask the AI Analysis tab about it; it sees the same numbers.
- **Net Worth Trend** — the two-line chart (Net worth in blue, Liquid net worth in green). The year you're viewing is shown month-by-month (Jan–Dec); each **prior year** is collapsed into a single point at the left using that year's December value (or its latest month with data). The points for the month you're viewing are ringed.

### AI Analysis

Ask questions about your finances in plain English (e.g. "How much did I spend on transportation in the past 3 months?" or "Which months did I save the most?") and get an auto-generated summary of your spending. This view talks to Claude (Anthropic's AI) directly from your browser.

- **You need a Claude API key.** Get one from the Anthropic Console (console.anthropic.com). Click **Setup** in the top-right of this view and paste it in. The key is stored only in this browser tab's memory (sessionStorage) and is cleared when you close the browser — you'll re-enter it next session. Your key is never saved to disk or sent anywhere except Anthropic's API.
- **Privacy note:** to answer questions, a summary of your financial data is sent to Anthropic's API — monthly income (by tax type), expenses by category, savings and investing by account, year-to-date tax totals, and your balance sheet (asset and liability names with amounts, net worth, liquid net worth) for the selected range. Nothing is stored on any server; the call goes straight from your browser to Anthropic.
- **Date range** — choose how far back to analyze (last 3 / 6 months, year to date, or all time). The line under the dropdown shows exactly which months that covers (e.g. "Covers Mar 2026 – Aug 2026") plus the approximate size and cost of each query — typically a couple of cents, using Claude Sonnet for accurate cross-referencing of your numbers. If you ask about a month outside that range, Claude will tell you it's out of range rather than saying there's no data — widen the range (e.g. to Year to Date) to include it.
- **Insights** — click **Generate** for a quick summary of your top spending categories, savings trend, patterns, and progress toward your budget goals. This only runs when you click it — opening the tab or changing the date range never queries the API on its own, so nothing costs you money without you asking for it.
- **Ask Claude** — a chat box for specific questions. It remembers earlier messages in the conversation, so you can ask follow-ups. **Clear chat** wipes the conversation. Both insights and chat are cleared when you close the browser.

### Both views

- **Month navigation** — use the ‹ › arrows in the header to review past or future months.
- **Backup & Restore** — export your data to a file and import it back, so you never lose it when switching browsers/computers or reformatting (see "How to use it" above). Backups include balance-sheet data.
- Delete any entry with the ✕ next to it.
