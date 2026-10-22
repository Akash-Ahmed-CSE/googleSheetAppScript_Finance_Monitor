# Finance Hub

A personal finance tracker for Google Sheets, built with Apps Script. It is designed for a salaried person in Bangladesh: BDT with lakh formatting, a July–June financial year, Provident Fund, Shonchoypotro, DPS and bKash.

Everything lives in one Google Sheet. There is no server and no third-party service.

## Features

- **Home dashboard:** pick a month and year, and income, spending, savings, budget, net worth, account balances and charts update.
- **Ledger:** one table for all money movements (Income, Expense, Transfer, Saving, Withdrawal, Invest).
- **Calculated balances:** account balances come from the Ledger, so nothing is typed twice.
- **Salary:** one row per month, with gross, net and financial year filled in automatically.
- **Investments:** maturity date and estimated value, with simple or compound interest.
- **DPS:** instalment schedule. Marking one **Paid** adds it to the Ledger.
- **Settings tab:** accounts, categories, budgets and rates are edited in the sheet, not in code.
- **Quick-add sidebar:** add entries from a form with dropdowns.
- **Automation:** daily email alerts (maturities, overdue DPS, budgets), monthly net-worth snapshot, PDF report and Drive backup.
- **Import:** brings data across from the older v2 workbook.

## Setup

1. Create a new Google Sheet.
2. Open **Extensions ▸ Apps Script**, replace `Code.gs` with the file from this repo, and save.
3. In **Project Settings**, set the time zone (for example Asia/Dhaka).
4. Reload the sheet and run **💰 Finance Hub ▸ Setup & tools ▸ First-time setup**.
5. Accept the permissions and choose **Yes** to enable automation. The DPS sync and amount cleaning need it.
6. In **Settings**, set opening balances and the tracking start date.

Setup is safe to re-run if something breaks. It keeps your data.

## How to use it

| Tab | Use it for |
|---|---|
| **Ledger** | Log income, expenses, transfers, savings, withdrawals and investments |
| **Salary** | Add one row each month |
| **Investments** | Register certificates, deposits and businesses |
| **DPS** | Mark instalments Paid |
| **Settings** | Change accounts, categories, budgets and options |

- Salary is added to your salary account automatically. Do not also log it in the Ledger.
- When you buy an investment, add it to **Investments** and log an **Invest** entry in the Ledger.
- Use **Finance Hub ▸ Setup & tools ▸ Health check** to find problems.

## Import from v2

Run **Setup & tools ▸ Import from old (v2) workbook** once on a fresh sheet and paste the old sheet's URL. Running it again creates duplicates.

## Notes

- Google Sheets only. The formulas use `ARRAYFORMULA`, `FILTER` and `UNIQUE`, which Excel does not fully support.
- Menus and the sidebar do not work in the Sheets mobile app.
- The script is a single file, `Code.gs`.
