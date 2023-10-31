### How to use
1. Navigate to `/cardless-ft`.
2. Click the button.
### Eligibility
If the toggle is on for the prototype, we'll assume the user is eligible.
### Frontend
We'll default to 3-day UK 1 Month Pro.
#### Claiming cardless FT
- New dummy page/route that has a barebones UI to claim the cardless free trial.
- This page shouldn't be indexed.
- It should have some sort of eligibility validation.
- Basic success & failure screens.
#### FT Extension
We'll use the existing billing info update flow in Titan and then we'll trigger the extension from the backend.
##### Data needed
- Whether or not the user is on a cardless free trial.