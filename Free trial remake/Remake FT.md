### Why
We want to add more free trial journeys and update some of the existing ones. Up until now, we have relied on the existing `FT3_SUSBCRIBE` and `FT7_SUBSCRIBE` journeys in ecomm-gate alone. Whenever we had a new journey in titan (e.g. search) we converted to either of the two ecomm-gate journeys. This allowed us to implement new journeys very quickly since all the work had to be done on titan only. 

However, it had a few downsides:
1. Different journeys (ft3, search) ended up using the same coupon under the hood, so it made data analysis difficult, as it wasn't obvious what journey they went through.
2. If we wanted to change the duration of a journey, we couldn't do it easily because there are only two underlying journeys on ecomm-gate that are shared between the titan journeys.


### Ideal solution
Our ideal solution is to have ecomm-gate be flexible enoug
Our proposal is to introduce a new eligibility query and a new purchase mutation that encapsulates all the free trial logic, keeping it separate from a normal subscription purchase. And also, keep the relationship between journey and coupon 1:1.

> Initially this work will only apply to the UK partnership.

### Main work
This remake is divided into two pieces of work:
* [[FT Eligibility]]
- [[New FT mutations]]

### Post-remake work
* Implement each journey in ecomm-gate