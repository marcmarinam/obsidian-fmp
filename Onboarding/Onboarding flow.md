The flow of onboarding is dictated by its state machine. Users can complete onboarding by skipping nodes, choosing different paths or just completing the happy path.

The happy path is:
1. Mother
2. Father
3. Maternal mother
4. Maternal father
5. Paternal mother
6. Paternal father

This happy path exists because of the underlying rules that decide the next step based on the current step and the nodes that have been skipped or added before.

The rules are, in order:
- If the spouse of the last added node is available, go there.
- If the mother of the current node is available, go there.
- If the father of the current node is available, go there.
- If the father of t