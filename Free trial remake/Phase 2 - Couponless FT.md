Phase 2 will be where we migrate to couponless free trials. With phase 1.5 done we have already taken care of storing FT purchases, now all we have to do is use that data.

### Main work

#### Eligibility
We'll begin by updating the new `isEligibleForFreeTrial` query to use the stored FT purchases data and all the existing checks (active sub, redeemed coupons, etc).

Even though we are moving to couponless, we still need to check for redeemed coupons, because so far all of our customers have been using them. Maybe we can stop doing that check at some point in the future, but for now, it's necessary.

#### Purchases
Once eligibility is in place, we can start moving away from coupons. Previously, the way we set the free trial length of a sub was by using a free trial type coupon. Now that we won't be using those, we need to set the `trialEndsAt` property when executing a purchase.

Storage of the purchased details has already been taken care of.

#### Extra
We will need to go over all the places where we expect an FT coupon and change the logic to rely only on the date.

The only places I can think of now are:
- `freeTrialDuration` property in a user's subscriptions
- `freeTrialDuration` property in purchase previews