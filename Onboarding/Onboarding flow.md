The flow of onboarding is dictated by its state machine. Users can complete onboarding by skipping nodes, choosing different paths or just completing the happy path.

The happy path is:
1. Mother
2. Father
3. Maternal mother
4. Maternal father
5. Paternal mother
6. Paternal father

This happy path exists because of the underlying rules that decide the next step based on the current step and the nodes that have been skipped or added before.

The next node will preferably be the spouse of the last added node, if it's not available, it will be the current node's mother, and if not, the father. If none of these is available, the same rules will apply to the spouse of the current node. If it still can't find a valid next step, onboarding is over.

Here's an example of the happy path:
![[onboarding-happy-path.excalidraw]]

Here's an example of an alternative path:
![[onboarding-alternative-path.excalidraw]]