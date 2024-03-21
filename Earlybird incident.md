### Timeline
- Bug was introduced on 18-07-2023
- Spotted & fixed on 13-03-2024
### Issue
Customers were able to convert free trial subscriptions to regular paid subscriptions for free. Subsequent renewals were also free. They could do this by starting a free trial in one domain and then redeeming earlybird on another.
### Cause
There was a mismatch between subscription plan and currency in both earlybird workflows (preview & purchase) that made it so the cost of the plan was 0.
### Customer impact
A total of 34 customers got free subscriptions.
### Business impact
Loss of revenue around £4400.
Customer support has to deal with the subscriptions.