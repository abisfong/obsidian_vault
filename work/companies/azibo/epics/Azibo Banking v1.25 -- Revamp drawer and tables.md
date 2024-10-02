*Created on: 4 September 2024, 2:15pm*
## Overview
1. Currently the tables have different columns and filters for `completed`, `pending`, `failed` and `scheduled`.
2. The drawer is only available for `completed` in accounts but is available for other tabs in outgoing payments however
3. the drawer shows limited information and is formatted differently in each instance.
## Stories
### Features
- [x] [[45696 - Category picked on billpay is not showing on transactions in bookkeeping]]
- [x] [[47964 - Consolidate transfer and transaction table UI]]
- [ ] [[48196 - Update category filters in bookkeeping page]]
- [x] [[47976 - Add scheduled tab in Accounts page]]
- [ ] [[48883 - Consolidate transaction and transfer drawer UI]]
### Bugs
- [ ] [[47491 - Manually created transactions that are unassigned a category and or property don't appear in Unassigned]]
## QA
- [Notion Bug Tracker](https://www.notion.so/azibo/3aa24ef2bc684f43b93af3c86f3ebf51?v=ce600fb4b446423081118235fc2af276)
## Notes
- QA deltas
	- Design deltas (what’s expected in the UI vs what we can offer)
		- Transfers can have all the same data
		- Transaction details
			- Memo not available in transfer data
				- Rename notes to memo
		- Payment timing
			- Transfer frequency available in all transfers
			- Only dates available are createdDt and updatedDt - no initiated or sent date available
		- Bookkeeping record
			- Notes are not in transfer data
				- Ignoring for now until update
			- Transfers do not have includeInScheduleE option
				- Remove includeInScheduleE
			- Updates
				- Add ability to update for scheduled transfers
		- Recipient details
			- Recipient details
		- Table sorts
			- Cannot sort transfers table by bookKeepingId (ask Ankur for update)
				- Disable sort
	- Design deltas (what’s in dev vs what we need)
		- Design title does not match per transfer type
		- Bookkeeping data is not present for transfers
		- Transfer data mismatched between transfers
	- Major bugs
		- Table sorts not working