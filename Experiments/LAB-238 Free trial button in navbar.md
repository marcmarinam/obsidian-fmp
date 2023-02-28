#### Experiment specifics

#### Toggle
Link: 

**Variants**
* Control: No free trial button in the navbar - 50%
* Variant 1 - Show the free trial button in the navbar - 50%

**Eligibility**
- Logged in users
- Never had a subscription

#### Implementation
The subscribe button is a very delicate component. It's rendered everywhere the navbar appears, so we need to be careful any changes we do won't crash the page it's being displayed in.

Internally, it uses a reducer (a form of state management) to handle the query that fetches the necessary information to know what to display and error handling. We won't need to alter this implementation. All we need to do is change/expand what we query for in order to determine if the user will see the new copy.

Currently, there are two queries being fired:
1.  The customer's active subscription
2.  The available plans for the customer

Based on the result of these queries the component reaches one of three states:
1.  SUBSCRIBE
2.  UPGRADE
3.  `null`

This is what determines the copy the customer sees, and where they navigate if they click it. `null` means the button is not displayed (there aren't any available plans to upgrade to).

We will need to fire an extra query to check for free trial eligibility. If we see the user is eligible for a free trial with regular eligibility (never subbed before) we will set the state of the button to a new one: FREE_TRIAL. If we are in that state, we will change copy, navigation, tracking, etc.