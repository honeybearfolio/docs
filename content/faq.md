---
title: "FAQ"
weight: 40
description: "Frequently Asked Questions about HoneyBear Folio."
---

# Frequently Asked Questions

### Where is my data stored?
HoneyBear Folio is a **local-first** application. Your data stays in a SQLite file on your computer. The app does not upload it.

The default file is `honeybear.db` inside the app data directory:

* **Linux**: `~/.local/share/com.honeybearfolio.honeybearfolio/honeybear.db` (or under `$XDG_DATA_HOME`)
* **macOS**: `~/Library/Application Support/com.honeybearfolio.honeybearfolio/honeybear.db`
* **Windows**: `%APPDATA%\com.honeybearfolio.honeybearfolio\honeybear.db`

You can keep more than one database. The session screen can create a file or open an existing one, and the sidebar shows which file is open. Use **Switch Session** to change it.

### Does it support automatic bank sync?
No. To maintain privacy and minimize dependencies on third-party aggregators (like Plaid or Yodlee), HoneyBear Folio relies on **file imports**. You can download CSV, JSON, or Excel files from your bank and import them using our robust column-mapping tool.

### Can I track investments?
Yes. Record buys and sells on an account. A trade stores the share leg and the matching cash leg. Quotes and daily prices come from Yahoo Finance and feed holdings, cost basis, gain or loss, the allocation chart, and the performance heatmap.

### Can I change what the dashboard shows?
Yes. **Customize** lets you drag, resize, remove, and add cards. **Reset layout** restores the default arrangement and leaves the date range and account filter alone. Each card can follow the dashboard date range or use its own, and can filter by account, category, payee, amount, and the other transaction fields. The arrangement is saved on this computer, not inside the database file.

### What is a goal?
A goal is a target amount funded by accounts and investments you choose. Each link can count all of that balance or a percentage of it. With a target date, a monthly contribution, or both, the goal is marked reached, on track, behind, or projected. Archive a goal to hide it without deleting it.

### Can I track a home, a car, or a loan?
Yes. **Assets** keeps a value history for things you own. **Liabilities** keeps a balance history for mortgages, loans, and other debts. Both are included in net worth.

### What is "Privacy Mode"?
Privacy Mode allows you to use the application in public or share screenshots without revealing your actual balances. When enabled, all numeric currency values are masked (e.g., `$*****`), but the currency symbol remains visible. Trends and percentage changes may still be shown.

### How do I backup my data?
Copy the open database file. The sidebar shows its path. You can also export JSON, CSV, Excel, or a PDF report for a period you choose. Copy the file before an import you may want to undo.

### Can I use multiple currencies?
Yes. You can set a base currency, and individual accounts and transactions can use another currency. Exchange rates come from Yahoo Finance. Under **Settings → General → Exchange Rates**, any rate can be replaced with one you enter.

### Which languages and themes are available?
The interface is available in English and Spanish. On a fresh install, language and formats follow your system, and you can change them in Settings. Themes are light, dark, high contrast, ink, or follow the system. You can also scale the type size.
