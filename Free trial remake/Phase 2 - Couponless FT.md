Phase 2 will be where we migrate to couponless free trials. With phase 1.5 done we have already taken care of storing FT purchases, now all we have to do is use that data.

### Main work
There are two main pieces of work in phase 2:
- Eligibility
- FT purchase
#### Eligibility
We'll need to update the new isEligibleForFreeTrial query to use the stored FT purchases data and all the existing checks (active sub, redeemed coupons, etc).
Even though we are moving to couponless, we still need to check for redeemed coupons, because so far all of our customers have been using them. Maybe we can stop doing that check at some point in the future, but 