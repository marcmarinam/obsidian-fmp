### Why
* Free trial is coupled with regular subscription purchases
* We have multiple free trial journeys, each with different durations and eligibility
* We don't want changes to subscription coupon logic to accidentally break FT or vice versa.

Our proposal is to introduce a new eligibility query and a new purchase mutation that encapsulates all the free trial logic, keeping it separate from a normal subscription purchase.

### Main work
* [[FT Eligibility]]
- [[New FT mutations]]