*Created on: 13 September 2024, 16:48*
## Tasks
- [x] Change check deposit item color on hover to peach
- [x] Add payment timing section
- [x] Add recipient information
- [x] Add account details
- [x] Update bookkeeping form to match new design
- [x] Add section styling
- [x] Show transfer bookkeeping record values
- [ ] Update recipient information to use recipient api (ask Ankur)
- [ ] Add edit and delete button for transfers
- [ ] Include transfer drawers for edit and delete in new transfer table
- [ ] Update title reflect transfer type
- [ ] GIVE JOSH UPDATE BY EOD (SEP 24) OF ESTIMATE
- [ ] Disable bookkeeping record for transfers except scheduled
- [ ] Remove memo data from transaction details
- [ ] Remove `includeInScheduleE` for transfers
- [ ] Add ability to update for scheduled transfers
- [ ] Add edit scheduled transfer drawer subpages and button
- [ ] Add delete scheduled transfer subpage and button
- [ ] Use next transfer date in scheduled transfers payment timing
## Deployment
- [ ] Create PR to develop
- [ ] Complete code review
- [ ] Merged to develop
- [ ] Create PR to production
- [ ] Complete code review
- [ ] Merged to production
# Blockers
- [[47964 - Consolidate transfer and transaction table UI]]
# Resources
- [Shortcut Ticket]()
- [Figma]()
## Questions
- Questions for meeting with Ankur and Assel
	- Recipient details
		- Ankur
			- Where can I find the institution name?
				- Can be found in recipient information via recipient API
		- Assel
			- What is institution name?
				- From recipient information
- Questions for meeting with JVL and Assel
	- Transaction details
		- All transfers have to and from account data. Do we want to do anything with the extra data in the drawers we're not using it?
	- Recipient details
		- Is the recipient the person receiving the transfer
	- Bookkeeping 
		- Notes/memo
			- Transfers do not have memo or notes at the moment. This will be updated by Ankur, but not in this iteration. Do we hide the data for now and leave the bookkeeping inputs?
			- Transactions have both notes and memos. At the moment, we're collecting notes, and then displaying it as the memo. Should we change their labels to match so the user doesn't get confused?
		- Unit
			- Transfers don't have unit data
	- Vendor/tenant and recipient details
		- Who will this be on transfers? The recipient?
## Notes
- 