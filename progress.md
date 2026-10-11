# Project 3: Prepare numeric features without leaking information — progress

**Guide status:** The starter files and project brief are published. Learner work on the open-ended checkpoints has not been verified, so the learning checklist starts unchecked.

Use this page across sessions. Check an item only after you have done it and can explain what you learned. If a step takes more than one sitting, leave it unchecked and write your next small move in the session log.

## Checkpoints

- [ ] **Inspect the numeric columns:** Compare pandas’ numeric-column list with a deliberate feature list and explain why `review_id` is excluded.
- [ ] **Read the baseline scaling:** Run the current all-rows demonstration and locate the learned mean, scale, and scaled values.
- [ ] **Create a tiny split:** Separate the invented rows into training and held-out groups for learning the preprocessing sequence; record how small this example is.
- [ ] **Avoid preprocessing leakage:** Fit a fresh scaler on training features only, then call `transform` on the held-out features using that same scaler.
- [ ] **Explain limits:** Describe what the split demonstrates and why six invented rows cannot support a claim about model performance.

## Completion criteria

- [ ] The chosen feature list contains meaningful measurements, not `review_id` or text labels.
- [ ] The practice program shows which mean and scale were learned.
- [ ] In the split-aware extension, only training feature rows are passed to `fit` or `fit_transform`.
- [ ] Held-out rows are processed with the already-fitted scaler using `transform`.
- [ ] The explanation calls this preprocessing practice, not a trained or evaluated prediction model.

## Session notes

Add one short entry whenever you stop. Keep your own observations here; blank entries are prompts, not claims about work already completed.

### Session 1
- Date:
- Checkpoint worked on:
- What I observed or changed:
- Question to resolve:
- Next small step:

### Session 2
- Date:
- Checkpoint worked on:
- What I observed or changed:
- Question to resolve:
- Next small step:

### Session 3
- Date:
- Checkpoint worked on:
- What I observed or changed:
- Question to resolve:
- Next small step:

### Later sessions
Add another heading when you need one.

## Optional extension

Compare standard scaling with a second scaling method on the same training split. Explain how the methods differ and why the comparison still says nothing about prediction quality without a model and appropriate evaluation.
