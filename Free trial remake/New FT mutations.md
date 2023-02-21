### Current solution
At the moment, whenever a user purchases a free trial, they call the `buySubscriptionPlan` mutation, which in turn calls the subscription purchase workflow. This is the same for a normal, fully paid subscription, making these two types of purchase coupled.

### Proposal
We want to create a new mutation and workflow that's free trial-specific, and that will handle all free trial journeys.