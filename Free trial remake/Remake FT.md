### Why
* Free trial purchases are coupled with regular subscription purchases.
* We have multiple free trial journeys, each with different durations and eligibility.
* We don't want changes to subscription coupon logic to accidentally break FT or vice versa.
* There's a many-to-1 relationship between journeys and coupons.

Our proposal is to introduce a new eligibility query and a new purchase mutation that encapsulates all the free trial logic, keeping it separate from a normal subscription purchase. And also, keep the logic to 1 journey = 1 coupon.

> Initially this work will only apply to the UK partnership.

### Main work
* [[FT Eligibility]]
- [[New FT mutations]]

### Post-remake work
* Implement each journey in ecomm-gate