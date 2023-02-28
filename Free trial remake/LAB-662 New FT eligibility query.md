### Current solution
Right now, there's only one query that returns if a member is eligible for a free trial. That free trial is the main 14-day free trial and there's no way to check eligibility for a different journey.

### Proposal
The new query we want to implement will take a journey as a parameter. Eligibility for every journey may differ.

### Implementation
To get this feature working, we'll have to create a new query. In our case the query doesn't need a new adapter or workflow to work, we can use the existing ones.

There are a few steps to creating a query:
1. Updating the schema. In this case `customer.graphql`
2. Creating a resolver for the query in `resolvers.ts`
3. Implementing the logic
4. Unit test it
   
Since this ticket is only about creating the query, we don't actually need to implement the eligibility for all journeys. We can do it only for the regular free trial as the first step.