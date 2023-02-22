### Why
We want to add more free trial journeys and update some of the existing ones. Up until now, we have relied on the existing `FT3_SUSBCRIBE` and `FT7_SUBSCRIBE` journeys in ecomm-gate alone. Whenever we have added a new journey in titan (e.g. search) we convert it to either of the two ecomm-gate journeys. This allows us to implement new journeys very quickly since all the work happens on titan only.

However, it has a few downsides:
1. Different journeys (ft3, search) end up using the same coupon under the hood, so it makes data analysis difficult, as it isn't obvious what journey a customer has used once the payment is done.
2. If we want to change the duration of a journey, we can't do it easily because there are only two underlying journeys on ecomm-gate that are shared between the titan journeys.

On ecomm-gate's side, there are other problems:
1. Free trial purchases use the same workflow as regular subscription purchases. So changes to coupon logic or

### Ideal solution
* Free trial purchases are coupled with regular subscription purchases.
* We have multiple free trial journeys, each with different durations and eligibility.
* We don't want changes to subscription coupon logic to accidentally break FT or vice versa.
* There's a many-to-1 relationship between journeys and coupons.
* Free trial purchases have sufficiently diverged from regular purchases that we think it justifies a new mutation and workflow.

Our proposal

Our proposal is to introduce a new eligibility query and a new purchase mutation that encapsulates all the free trial logic, keeping it separate from a normal subscription purchase. And also, keep the relationship between journey and coupon 1:1.

> Initially this work will only apply to the UK partnership.

### Main work
This remake is divided into two pieces of work:
* [[FT Eligibility]]
- [[New FT mutations]]

### Post-remake work
* Implement each journey in ecomm-gate