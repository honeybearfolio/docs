---
title: "Goals"
weight: 8
description: "Track a target funded by accounts and investments."
---

**Goals** in the sidebar tracks a target amount against the accounts and investments you link to it. Progress is saved in the open database.

## Creating a goal

1. Open **Goals** and click **New goal**.
2. Enter a name and a target amount greater than zero.
3. Optionally set a currency. An empty currency uses the app currency. Amounts on the page are shown in the app currency.
4. Optionally set a target date, a monthly contribution, notes, and a color.
5. Under **Funding**, add one or more sources. Each source uses an allocation from 1 to 100 percent. The default is 100.
6. Save the goal.

### Funding sources

- **Account.** The current amount is that account's cash balance plus the market value of its holdings, multiplied by the allocation.
- **Investment.** Pick a ticker. Leave the account as **All accounts**, or limit the holding to one account. The current amount is the market value, multiplied by the allocation.

If a linked investment is already included in a linked account, both amounts are counted. The goal warns you when that happens.

## How progress is judged

The page shows how much of the target is funded, how much remains, and a status:

- **Reached.** The linked amounts meet the target.
- **On track** or **Behind**, when the goal has a target date. With a monthly contribution, the status compares the date that contribution would finish the goal with the target date. Without one, it compares the amount funded with the share of the target that the elapsed time would suggest. Either way, the card shows the monthly amount that would finish on time.
- **Projected**, when there is a monthly contribution and no target date. The card shows the date that contribution would reach the target.
- **No date**, when neither a target date nor a monthly contribution is set.

## Archiving and deleting

**Archive** hides a goal from the active list without removing it. **Show archived** brings those goals back, and **Restore** makes one active again. **Delete** removes the goal. The summary at the top counts active goals, how much they have funded, and how many are on track.
