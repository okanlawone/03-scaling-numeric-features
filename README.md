# Project 3: Prepare numeric features without leaking information

Choose measurements intentionally, exclude numeric identifiers, and extend the scaling demonstration to fit preprocessing on training rows before transforming held-out rows.

**Repository:** [okanlawone/03-scaling-numeric-features](https://github.com/okanlawone/03-scaling-numeric-features)  
**Course index:** [ai-engineering-journey](https://github.com/okanlawone/ai-engineering-journey)

## What you will learn

- Recognize that numeric storage does not make an identifier a useful measurement.
- Explain what `StandardScaler` learns from the data passed to `fit`.
- Practice the safe fit-on-training, transform-on-held-out-data sequence without training a model.

## Project format

This is an open-ended, multi-session project. The starter program demonstrates the core idea; your work is to inspect it, extend it, and explain the choices. There is no one-day deadline. Pick up at the next unchecked item in [`progress.md`](progress.md). The detailed background and project brief are in [`lesson.md`](lesson.md).

## Checkpoints

- [ ] **Inspect the numeric columns:** Compare pandas’ numeric-column list with a deliberate feature list and explain why `review_id` is excluded.
- [ ] **Read the baseline scaling:** Run the current all-rows demonstration and locate the learned mean, scale, and scaled values.
- [ ] **Create a tiny split:** Separate the invented rows into training and held-out groups for learning the preprocessing sequence; record how small this example is.
- [ ] **Avoid preprocessing leakage:** Fit a fresh scaler on training features only, then call `transform` on the held-out features using that same scaler.
- [ ] **Explain limits:** Describe what the split demonstrates and why six invented rows cannot support a claim about model performance.

## Run the starter project

Clone this project repository, then run these commands from its root:

```bash
git clone https://github.com/okanlawone/03-scaling-numeric-features.git
cd 03-scaling-numeric-features
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python main.py
```

The code reads its CSV from the project folder, so it does not depend on your terminal’s current directory. The small CSV is invented practice data; it is not real customer data. See [`lesson.md`](lesson.md) for the data and training-data distinction.

## What counts as complete

Use the checklists in `lesson.md` and `progress.md`. A project is ready to close when the required behavior works, you can explain why the choices make sense, and the data limitations are documented. Optional extensions can wait for a later version.

**Optional extension:** Compare standard scaling with a second scaling method on the same training split. Explain how the methods differ and why the comparison still says nothing about prediction quality without a model and appropriate evaluation.
