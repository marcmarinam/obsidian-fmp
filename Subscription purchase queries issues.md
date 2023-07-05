#### Original plan
The plan was to make the `SubscriptionPlan` schema object have a `SubscriptionPurchasePreview` as a property.
#### Issues
Adding that property to the schema introduced self-reference. 

`SubscriptionPlan` -> `SubscriptionPurchasePreview` -> `PurchasePreview` -> `SubscriptionPlan`.

This didn't appear to be a problem in 