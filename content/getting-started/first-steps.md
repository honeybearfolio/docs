---
title: "First Steps"
weight: 20
description: "First steps with HoneyBear Folio."
---

## Opening a database

The first screen asks which database to use.

- **Create New Session** saves a new SQLite file. The suggested name is `honeybear.db`.
- **Open Existing** opens a `.db` or `.sqlite` file you already have.
- **Recent Sessions** lists files you have opened before.

The sidebar shows the open file. Use **Switch Session** there to create, open, or change databases. Copy that file before an import you may want to undo.

On a fresh install, language, base currency, number format, date format, and the first day of the week are taken from your system. Change them later in **Settings**:

- **General**: base currency, the database file, and exchange rates. Any rate can be replaced with one you enter.
- **Formats**: number format, date format, and the first day of the week.
- **Customization**: light, dark, high contrast, ink, or follow the system, and the type size. Language (English or Spanish) is in Settings as well.

You then land on the **Dashboard**.

## Creating an Account

Accounts are listed in the sidebar.

1. Click **New Account** (the **+** next to the accounts list).
2. Fill in:
    * **Account Name**: for example, "Main Checking".
    * **Initial Balance**: the starting balance. Leave it blank for 0.00. A non-zero balance is stored as an opening transaction.
    * **Currency**: optional. If left empty, the account uses your base currency.
3. Save the account.

## Creating a Transaction

1. Select the account in the sidebar.
2. Click **New Transaction**.
3. Choose the type:
    * **Cash**: income, expenses, and transfers.
        * **Date**, **Payee**, **Category**, optional **Notes**, and **Amount**. Use a positive amount for income and a negative amount for an expense.
        * A transfer between accounts uses the Transfer category and records the other side of the move.
    * **Investment**: a buy or a sell.
        * **Buy / Sell**, **Date**, **Ticker** (for example AAPL or BTC-USD), **Shares**, **Price**, **Fee**, and optional **Notes**.
        * The trade records the share leg and the matching cash leg.
4. Save the transaction.

From the account you can search, edit, duplicate, and delete transactions.
