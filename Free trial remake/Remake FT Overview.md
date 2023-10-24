### Why
We want to add more free trial journeys and update some of the existing ones. Up until now, we have relied on the existing `FT3_SUSBCRIBE` and `FT7_SUBSCRIBE` journeys in ecomm-gate alone. Whenever we have added a new journey in titan (e.g. search) we convert it to either of the two ecomm-gate journeys. This allows us to implement new journeys very quickly since all the work happens on titan only.

However, it has a few downsides:
1. Different journeys (ft3, search) end up using the same coupon under the hood, so it makes data analysis difficult, as it isn't obvious what journey a customer has used once the payment is done.
2. If we want to change the duration of a journey, we can't do it easily because there are only two underlying journeys on ecomm-gate that are shared between the titan journeys.

On ecomm-gate's side, there are other problems:
1. Free trial purchases use the same two workflows as regular subscription purchases. So changes to business logic in those workflows can have unintended consequences.
2. Eligibility for purchasing free trials is quite inflexible. We want to loosen the restrictions placed on users, and we'd prefer to have ecomm-gate be the source of truth rather than titan.
### Ideal solution
Our proposal is to introduce new queries, mutations and workflows exclusive to free trial purchases. That will allow us to isolate all the special logic we want to define and be assured that changes to either normal or free trial purchases don't affect one another by accident.
### Discussed solution
Instead of breaking apart the workflows, we can break apart the `getSubscriptionPlanData` and `getSubscriptionChangeData`. They are currently pulling too much weight, and having one of these functions specifically for free trial could be enough.

We can create a new `getFreeTrialData` function that has similar responsibilities to the two mentioned before. This function could be called by the `experimentalFreeTrialPurchaseWorkflow`.
#### Main work
This remake is divided into two pieces of work:
- [LAB-662 New FT eligibility query](LAB-662%20New%20FT%20eligibility%20query.md)
- [LAB-663 New FT mutations](LAB-663%20New%20FT%20mutations.md)
### Post-remake work
* Implement each journey in ecomm-gate