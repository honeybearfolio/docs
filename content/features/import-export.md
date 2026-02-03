---
title: "Importing and Exporting Data"
weight: 10
description: "Learn how to import transactions from other sources and export your data for backup or analysis."
---

HoneyBear Folio is designed to be interoperable. You can bring your existing data with you and take your data out at any time.

## Importing Data

You can import transactions from various file formats. This is useful for migrating from other tools or importing bank statements.

### Supported Formats

HoneyBear Folio supports importing files in the following formats:

- **CSV (`.csv`)**: Comma-Separated Values.
- **JSON (`.json`)**: JavaScript Object Notation.
- **Excel (`.xlsx`, `.xls`)**: Microsoft Excel Spreadsheets.

### How to Import

1. Open the **Import** modal (usually found in the Sidebar or Settings).
2. **Select your file** or drag and drop it into the upload area.
3. The system will attempt to **auto-map columns** based on the headers in your file.
4. Review the mapping. You can manually assign columns to the following fields:
   - **Date**: Transaction date.
   - **Payee**: Merchant or description.
   - **Amount**: Transaction value.
   - **Category**: Expense or income category.
   - **Notes**: Additional details.
   - **Account**: The account associated with the transaction.
   - **Ticker / Symbol**: For investment transactions.
   - **Shares / Quantity**: Number of units.
   - **Price**: Price per unit.
   - **Fee**: Transaction fees.
   - **Currency**: Transaction currency.

### Automatic Mapping Logic

The importer tries to guess the correct columns by looking for keywords in your file headers (case-insensitive):

- **Date**: `date`
- **Payee**: `payee`, `description`, `merchant`
- **Amount**: `amount`, `value`
- **Category**: `category`
- **Notes**: `note`, `memo`
- **Account**: `account`, `acc`
- **Ticker**: `ticker`, `symbol`
- **Shares**: `shares`, `quantity`, `qty`
- **Price**: `price`
- **Fee**: `fee`, `commission`
- **Currency**: `currency`, `curr`

### JSON Support

For JSON files, the importer looks for an array of transaction objects. It supports:
- A top-level array: `[...]`
- A `transactions` field: `{ "transactions": [...] }`
- A `data` field: `{ "data": [...] }`

## Exporting Data

You can export your data for backup purposes or for further analysis in other tools.

### Supported Formats

- **JSON (`.json`)**: Best for full backups and interoperability.
- **CSV (`.csv`)**: Best for importing into spreadsheet software like Google Sheets or Excel.
- **Excel (`.xlsx`)**: Generates a native Excel file with multiple sheets.

### Export Details

#### JSON Export
The JSON export includes both **Accounts** and **Transactions**.
- Transaction references to Account IDs are replaced with **Account Names** for better readability and portability.
- The file includes a metadata field `exportDate`.

#### CSV Export
The CSV export generates a flat list of transactions with the following columns:
`Date`, `Account`, `Payee`, `Category`, `Amount`, `Notes`, `Ticker`, `Shares`, `Price`, `Fee`, `Currency`.

#### Excel Export
The Excel export creates a specific `.xlsx` file containing two sheets:
1. **Transactions**: The list of all your transactions.
2. **Accounts**: A list of your account definitions.
