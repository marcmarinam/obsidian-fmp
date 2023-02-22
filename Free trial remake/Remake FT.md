### Why
We want to add/update the existing free trial journeys. Up until now, we have relied on the existing `FT3_SUSBCRIBE`  and 
### Why
* Free trial purchases are coupled with regular subscription purchases.
* We have multiple free trial journeys, each with different durations and eligibility.
* We don't want changes to subscription coupon logic to accidentally break FT or vice versa.
* There's a many-to-1 relationship between journeys and coupons.
* Free trial purchases have sufficiently diverged from regular purchases that we think it justifies a new mutation and workflow.

Our proposal is to introduce a new eligibility query and a new purchase mutation that encapsulates all the free trial logic, keeping it separate from a normal subscription purchase. And also, keep the relationship between journey and coupon 1:1.

> Initially this work will only apply to the UK partnership.

### Main work
This proposal is divided into two pieces of work:
* [[FT Eligibility]]
- [[New FT mutations]]

### Post-remake work
* Implement each journey in ecomm-gate