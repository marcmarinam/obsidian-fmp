In order to send the correct email to each user in the experiment we need to know which variant they are in **before** we even launch the experiment. The problem is that we can't know what variant a user will land on before the 50/50 rollout is active.

The only way to get the variant for each user and have it not change is to have the experiment toggle enabled throughout the free weekend. That would mean we are showing the experiment to users before we actually want to. The solution is a second toggle.

We can create a second toggle that controls whether or not the experiment is fully enabled. It could be an operational toggle. This is what the setup would look like.

During the free weekend:
- `master-toggle`: Off.
- `experiment-toggle`: UK 50/50.
``
When we want to launch the experiment:
- `master-toggle`: On.
- `experiment-toggle`: UK 50/50.

It's important that we don't change the rollout for the experiment toggle. I imagine any change to it will change what variants users are in.