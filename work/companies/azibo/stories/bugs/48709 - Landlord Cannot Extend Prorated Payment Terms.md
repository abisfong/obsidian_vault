*Created on: 19 September 2024, 15:37*
## Tasks
- [x] Use repro instructions to recreate bug
- [x] Look at form validation, which may be causing the issue
## Deployment
- [ ] Create PR to develop
- [ ] Complete code review
- [ ] Merged to develop
- [ ] Create PR to production
- [ ] Complete code review
- [ ] Merged to production
# Blockers
- 
# Resources
- [Shortcut Ticket](https://app.shortcut.com/azibo-inc/story/48709/landlord-prod-extending-payment-terms-can-not-extend-prorated-payment-terms)
## Questions
- 
## Notes
- Payment term initial state had duplicate code. I consolidated it and assigned the correct values when extending terms. The issue was that `isFirstMonthProrated` as being set to true, which it can't be for an extended payment term. `isLastMonthProrated` was also being set to true, but 