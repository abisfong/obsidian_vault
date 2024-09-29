*Created on: 13 September 2024, 16:48*
## Tasks
- [x] Change check deposit item color on hover to peach
- [x] Add payment timing section
- [x] Add recipient information
- [x] Add account details
- [x] Update bookkeeping form to match new design
- [x] Add section styling
- [x] Show transfer bookkeeping record values
- [x] Update recipient information to use recipient api (ask Ankur)
- [x] Update title to reflect transfer type
- [ ] Use front or back of check image title for drawer when in attachment view
- [x] GIVE JOSH UPDATE BY EOD (SEP 24) OF ESTIMATE
- [x] Disable bookkeeping record for transfers except scheduled
- [x] Remove memo data from transaction details
- [x] Remove `includeInScheduleE` for transfers
- [x] Add ability to update scheduled transfers
- [x] Add edit scheduled transfer drawer subpages and button
- [x] Add delete scheduled transfer subpage and button
- [x] Use next transfer date in scheduled transfers payment timing
- [ ] Add alert when bookkeeping record is disabled
- [x] Show frequency for selected transfers in design
- [ ] Fix `Payment Timing` date label
- [ ] Internal transfers: ACH pull and next day pull, reverse from and to accounts, and amount sign
- [ ] For check deposits, amount should be positive
- [ ] If payee or payer match accountId, use the current users info for recipient details to avoid making calls
- [ ] If payee is different than the LL's account id, then it is a BillPay recipient
- [ ] Remove recipient details from funds transfer
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
- Memo for scheduled transfers is saved under description. Users can edit description
- Work section by section