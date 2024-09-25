*Created on: 4 September 2024, 12:15pm*

We're currently using separate tables for transfers and transactions. Join the table UI into one.
## Tasks
- [x] Add `Contact` column to both tables
- [x] Add `Incoming/Outgoing` filter to both tables (replaces `Type` filter)
- [x] Add `Type` to transaction table
- [x] Add `View` button to transfers table
- [x] Add `Property` column to transfers table
- [x] Indicate outgoing transfer with red, negative numbers
- [x] Add `Search` filter to transfers table
- [x] Add `Date range` filter to transfers table
- [x] Add ability to increase size of filter on screen size > tablet
- [x] Increase size of `Search` filter
- [x] Implement use of `transactionDisplayType` mentioned [here](https://zibo-workspace.slack.com/archives/D03G7BFBQK1/p1724706768022369)
- [x] Make these changes in accounts page only by duplicating code and maintaining old code in bookkeeping page and outgoing payments
- [x] Remove selection checkboxes
- [x] Update incoming/outgoing filter to use BE updates and include transfer properties
- [x] Remove contact sorting in transfer table
- [x] Update sorting filters to match design
- [x] Remove category filter from transfer table
- [x] Update sorting filters to pass PGS sorting params
- [ ] Update property filter to send `properties: string[]` rather than `propertyIds`
## Deployment
- [ ] Create PR to develop
- [ ] Complete code review
- [ ] Merged to develop
- [ ] Create PR to production
- [ ] Complete code review
- [ ] Merged to production
# Blockers
- None
## Resources
- [Shortcut Ticket](https://app.shortcut.com/azibo-inc/story/47964/fe-consolidate-transfer-and-transaction-table-ui)
* [Figma](https://www.figma.com/design/VxbEjaadB0rH9S0gdhuLSr/Banking-View-Transactions?node-id=405-34087&node-type=FRAME&t=ur2ts43Y2UGtJcQE-0)

## Questions
- Will the bookkeeping table be updated by the growth pod?
	- *JVL: Yes*

## Notes
- **These updates are only within the accounts page**