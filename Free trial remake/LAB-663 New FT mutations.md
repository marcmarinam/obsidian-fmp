### Current solution
At the moment, whenever a user purchases a free trial, they call the `buySubscriptionPlan` mutation, which in turn calls the subscription purchase workflow. This is the same for a normal, fully paid subscription, making these two types of purchase coupled.

### Proposal
We want to create two new mutations and workflows that will be free trial-specific and will handle all free trial journeys.

### Implementation
Instead of creating two new mutations and workflows, we will start by creating a new function that validates data before a free trial purchase. The function that is used at the moment is 