#### Original plan
The plan was to make the `SubscriptionPlan` schema object have a `SubscriptionPurchasePreview` as a property.

#### Issues
Adding that property to the schema introduced self-reference. 

`SubscriptionPlan` -> `SubscriptionPurchasePreview` -> `PurchasePreview` -> `SubscriptionPlan`.

This didn't appear to be a problem in `codegen-types.ts` but it was in `codegen-mocks.ts`.

#### Alternative solutions
- Creating a new top-level query called `previewSubscriptionPlanPurchases` that takes multiple plan ids as input.
- Add a new `Preview` type that doesn't contain a plan inside it. Since we want it to be a child of `SubscriptionPlan`.