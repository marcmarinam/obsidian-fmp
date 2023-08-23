### Onboarding reminder email
Info we need:
1. Knowing that a user has abandoned onboarding.
2. Knowing when the user abandoned onboarding.

### Storage options

#### Non-DB storage

Instead of storing the onboarding state, we can regenerate it and place users back on the next onboarding step based on the nodes they have created.

##### Product considerations
1. Do we want to keep track of what nodes were skipped? If a user comes back to onboarding and the nodes they skipped are available again is it a big deal?



#### DB storage
