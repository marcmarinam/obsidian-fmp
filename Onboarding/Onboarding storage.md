### Onboarding reminder email
Info we need:
1. Knowing that a user has abandoned onboarding.
2. Knowing when the user abandoned onboarding.
### Storage options
#### Non-DB storage
Instead of storing the onboarding state, we can regenerate it and place users back on the next onboarding step based on the nodes they have created.
##### Potential issues
1. Do we want to keep track of what nodes were skipped? If a user comes back to onboarding and the nodes they skipped are available again is it a big deal?
2. Added complexity due to having to interpret tree
#### DB storage
TODO

#### Completed onboarding
1. What counts as completed onboarding? 
	1. When they leave and create >1 extra nodes? 
	2. Any tree change outside of onboarding?
	3. When they get to the success screen?
	4. When they reach 3 generations up?
2. Do we only remind users to complete onboarding on their first tree or any tree they create?