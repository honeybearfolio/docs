---
title: "FAQ"
weight: 40
---

# Frequently Asked Questions

### Where is my data stored?
HoneyBear Folio is a **local-first** application. All your data is stored in a single SQLite database file (`honeybear.db`) on your computer. We do not store your data on any cloud servers.

**Path locations:**
* **Linux**: `~/.local/share/honeybear-folio/honeybear.db`
* **macOS**: `~/Library/Application Support/honeybear-folio/honeybear.db`
* **Windows**: `%APPDATA%\honeybear-folio\honeybear.db`

### Does it support automatic bank sync?
No. To maintain privacy and minimize dependencies on third-party aggregators (like Plaid or Yodlee), HoneyBear Folio relies on **file imports**. You can download CSV, JSON, or Excel files from your bank and import them using our robust column-mapping tool.

### Can I track investments?
Yes! You can create Investment Accounts and add tickers (e.g., AAPL, VTI). The app fetches real-time quotes and daily historical prices via Yahoo Finance to calculate your portfolio's market value.

### What is "Privacy Mode"?
Privacy Mode allows you to use the application in public or share screenshots without revealing your actual balances. When enabled, all numeric currency values are masked (e.g., `$*****`), but the currency symbol remains visible. Trends and percentage changes may still be shown.

### How do I backup my data?
Since your data is a single file (`honeybear.db`), you can simply copy this file to a safe location (external drive, cloud storage folder, etc.). The application also has a built-in export feature to save a backup of the database.

### Can I use multiple currencies?
Yes. You can set a base currency for the application, but individual accounts and transactions can be in any currency. The app will automatically fetch exchange rates to convert everything to your base currency for net worth reporting.
