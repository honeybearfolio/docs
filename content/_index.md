---
title: "HoneyBear‑Folio"
description: "Documentation for HoneyBear‑Folio"
date: 2026-02-04
draft: false
weight: 1
---

## About the Project

**HoneyBear Folio** is a local-first personal finance app for the desktop. Accounts, investments, and net worth stay in a SQLite file on your machine. It is built with **Tauri** and **React**, and it does not require an account or a remote server.

### What it covers

- **Dashboard.** Net worth, income against expenses, spending by category, how assets are split, and a cash-flow diagram. Arrange the cards, hide accounts, and give any card its own date range and filters.
- **Goals.** A target funded by the accounts and investments you link to it, with a status for whether you are on track.
- **Investments.** Holdings, cost basis, and gain or loss. Quotes and daily prices come from Yahoo Finance.
- **Transactions.** Cash accounts, transfers between accounts, and brokerage trades. A buy or sell records the share leg and the matching cash leg.
- **Scheduled transactions and rules.** Recurring items wait until you apply them. A rule can fill in fields while you type a transaction and again during import.
- **Assets and liabilities.** A value history for things you own, and a balance history for mortgages, loans, and other debts. Both are included in net worth.
- **FIRE calculator.** Starts from your balances, spending, and savings, then projects a target with a single path and a Monte Carlo range.
- **Import and export.** CSV, Excel, or JSON in, with column mapping and preview. JSON, CSV, Excel, or a PDF report out.

You can keep more than one database and switch from the sidebar. Accounts and transactions can use different currencies. The interface is available in English and Spanish, and an optional assistant uses [Ollama](https://ollama.com) on your computer. It can look up accounts, transactions, holdings, assets, liabilities, and goals.

Start with [Installation](getting-started/installation/) and [First Steps](getting-started/first-steps/), or browse [Features](features/).
