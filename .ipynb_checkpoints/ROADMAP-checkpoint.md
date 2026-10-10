# 30-Day GCI World Competition Plan: Become an Outstanding Student

Your goal is not just to submit a model. It is to build a strong, reproducible machine-learning solution for the GCI World 2026 in-class competition and maximize your chance of being selected as an Outstanding Student.

I've based this plan on your uploaded In-Class Competition Tutorial from the University of Tokyo's Matsuo-Iwasawa Laboratory.

## 1. Understand what you must achieve

According to the tutorial, the course requirements are:

| Requirement          | Honors                 | Outstanding            |
| -------------------- | ---------------------- | ---------------------- |
| Attendance surveys   | 7+                     | 7+                     |
| Homework points      | 14+                    | 14+                    |
| Final assignment     | Pass                   | Pass                   |
| Competition          | Participation required | Participation required |
| Competition ranking  | —                      | Top 10%                |
| Overall course score | —                      | Top 20%                |

The tutorial says that you must participate in the competition to become an Honors or Outstanding Student, and Outstanding selection requires both the competition ranking and overall-score criteria. These are selection criteria, not a guarantee of selection.&#x20;

competition_tutorial.pdf



Your competition task is to predict the probability that a customer will default on a loan. The tutorial recommends an iterative workflow: establish a baseline, add features, try different models, tune hyperparameters, and create additional features.&#x20;

competition_tutorial.pdf



## Your 30-day mission

# Top 10%

Competition ranking target

# Top 20%

Overall course-score target

## Reproducible

Documented model and code

## Measured gains

Every experiment compared fairly

Important deadline note: the tutorial lists the competition deadline as November 20, 2026, at 1:00 AM UTC, which is 7:00 AM Bangladesh Standard Time on November 20. A 30-day plan starting October 10 ends November 8, giving you a buffer for final improvements and submission. Verify the deadline and submission rules on Omnicampus before relying on this date.&#x20;

competition_tutorial.pdf



## 2. Your daily schedule

Plan for approximately 3 hours per day, with 4-hour sessions on important experiment and review days.

### Daily 3-hour routine

30 minutes — Learn

Understand one ML concept or model.

90 minutes — Implement

Code, inspect data, train models, and run experiments.

30 minutes — Evaluate

Compare scores and record what worked.

30 minutes — Document

Write experiment notes, next steps, and code changes.

## 3. The complete 30-day competition roadmap

The plan starts on October 10, 2026, and ends on November 8, 2026. The tasks build on the competition tutorial's workflow, with additional practical steps for reliable validation, experiment tracking, and code quality.

### Phase 1 — Setup and understand the data

Days 1–5 · October 10–14 · Goal: establish a working baseline.

| Day / date | Daily task                | What to do                                                                                                         | Expected output         | Time |
| ---------- | ------------------------- | ------------------------------------------------------------------------------------------------------------------ | ----------------------- | ---- |
| 1 · Oct 10 | Environment setup         | Download the competition folder, upload it to Google Drive, open `tutorial.ipynb`, and correct the data path.      | Notebook runs correctly | 3 h  |
| 2 · Oct 11 | Baseline submission       | Run all tutorial cells, create `submission.csv`, and submit it on Omnicampus. Save your score.                     | First valid submission  | 3 h  |
| 3 · Oct 12 | Read competition rules    | Read `README.ipynb`; identify evaluation rules, target, files, and submission requirements.                        | Competition notes       | 3 h  |
| 4 · Oct 13 | Understand the dataset    | Inspect `HomeCredit_columns_descriptions.xlsx`, dataset shapes, column names, data types, and target distribution. | Data dictionary notes   | 3 h  |
| 5 · Oct 14 | Exploratory data analysis | Check missing values, duplicates, numerical distributions, categorical frequencies, and target imbalance.          | EDA notebook and charts | 4 h  |

Phase checkpoint: You should have a working baseline submission, understand what you are predicting, and know the major data-quality problems.

### Phase 2 — Build your validation and feature-engineering skills

Days 6–10 · October 15–19 · Goal: understand what drives the predictions.

| Day / date  | Daily task                       | What to do                                                                                               | Expected output                 | Time |
| ----------- | -------------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------- | ---- |
| 6 · Oct 15  | Establish validation             | Create a reproducible train/validation split; use stratification if appropriate for the target.          | Fixed validation setup          | 3 h  |
| 7 · Oct 16  | Understand the evaluation metric | Identify the official competition metric. Choose a local validation metric that matches it.              | Evaluation function             | 3 h  |
| 8 · Oct 17  | Missing-value analysis           | Compare missingness by column and target; test sensible imputation methods within the training pipeline. | Missing-value experiment        | 4 h  |
| 9 · Oct 18  | Categorical features             | Explore category frequencies and compare appropriate encoding strategies.                                | Encoding experiment             | 4 h  |
| 10 · Oct 19 | Numerical features               | Inspect skew, ranges, outliers, and correlations. Test only justified transformations.                   | Improved preprocessing pipeline | 3 h  |

Phase checkpoint: You can evaluate a model locally before submitting it. This is essential because leaderboard feedback alone does not tell you whether a change genuinely improves generalization.

### Phase 3 — Try stronger models

Days 11–15 · October 20–24 · Goal: find a model that beats the baseline.

| Day / date  | Daily task          | What to do                                                                                                | Expected output           | Time |
| ----------- | ------------------- | --------------------------------------------------------------------------------------------------------- | ------------------------- | ---- |
| 11 · Oct 20 | Logistic regression | Build a simple benchmark using appropriate preprocessing and regularization.                              | Logistic regression score | 3 h  |
| 12 · Oct 21 | Random forest       | Train a tree-based baseline and compare it with logistic regression.                                      | Model comparison          | 3 h  |
| 13 · Oct 22 | Gradient boosting   | Try a suitable boosting model, such as XGBoost, LightGBM, or CatBoost if available.                       | Boosting score            | 4 h  |
| 14 · Oct 23 | Compare models      | Evaluate all models on the same split and metric. Check for overfitting and reproducibility.              | Ranked model table        | 3 h  |
| 15 · Oct 24 | Error analysis      | Inspect validation predictions, false positives and false negatives where useful, and feature importance. | Error-analysis notes      | 4 h  |

Phase checkpoint: Select your strongest model based on local validation, not just the public leaderboard.

### Phase 4 — Feature engineering and hyperparameter tuning

Days 16–20 · October 25–29 · Goal: improve the strongest model systematically.

| Day / date  | Daily task                 | What to do                                                                                                 | Expected output               | Time |
| ----------- | -------------------------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------- | ---- |
| 16 · Oct 25 | Create meaningful features | Test domain-informed ratios, differences, counts, or grouped features when justified by available columns. | Feature-engineering version 1 | 4 h  |
| 17 · Oct 26 | Test feature sets          | Add feature groups incrementally and compare against the same validation baseline.                         | Feature ablation results      | 3 h  |
| 18 · Oct 27 | Hyperparameter tuning      | Tune a few important parameters using random search or a small grid. Keep the validation method fixed.     | Best parameters so far        | 4 h  |
| 19 · Oct 28 | Improve regularization     | Check model complexity, overfitting, early stopping if supported, and training stability.                  | More robust model             | 3 h  |
| 20 · Oct 29 | Reproducibility audit      | Rerun the leading experiment with fixed seeds and record its settings, metric, and runtime.                | Reliable experiment record    | 3 h  |

The tutorial specifically suggests adding features, trying models such as AdaBoost, XGBoost, CatBoost and LightGBM, tuning parameters, and creating additional features.&#x20;

competition_tutorial.pdf



### Phase 5 — Refine, ensemble, and compete

Days 21–25 · October 30–November 3 · Goal: turn the best experiments into a competitive solution.

| Day / date  | Daily task                  | What to do                                                                                                          | Expected output             | Time |
| ----------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------- | --------------------------- | ---- |
| 21 · Oct 30 | Improve feature engineering | Investigate additional features and interactions suggested by EDA and the column descriptions.                      | Feature version 2           | 4 h  |
| 22 · Oct 31 | Try ensembling              | Blend or average predictions from complementary models if validation supports it.                                   | Ensemble comparison         | 4 h  |
| 23 · Nov 1  | Tune the finalist           | Run a focused search around the best model's promising parameters.                                                  | Finalist configuration      | 4 h  |
| 24 · Nov 2  | Submit and compare          | Generate a fresh submission and compare its leaderboard result with earlier submissions.                            | Updated leaderboard record  | 3 h  |
| 25 · Nov 3  | Investigate score gaps      | Compare local validation with public leaderboard performance; look for leakage, split differences, and overfitting. | Improvement hypothesis list | 3 h  |

Rule for this phase: Never keep an experiment merely because it is more complicated. Keep it if it improves a trustworthy validation result or offers another well-supported benefit.

### Phase 6 — Finalize, document, and submit correctly

Days 26–30 · November 4–8 · Goal: deliver a strong model and complete code submission.

| Day / date | Daily task                 | What to do                                                                                                                                         | Expected output                     | Time |
| ---------- | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- | ---- |
| 26 · Nov 4 | Consolidate experiments    | Compare your best individual models and ensemble. Freeze a candidate for final evaluation.                                                         | Selected candidate                  | 3 h  |
| 27 · Nov 5 | Full training pipeline     | Rebuild the chosen pipeline cleanly and retrain according to the competition rules.                                                                | Final training notebook             | 4 h  |
| 28 · Nov 6 | Test submission generation | Run the notebook end-to-end, check prediction count, column names, file format, and finite probabilities.                                          | Verified `submission.csv`           | 3 h  |
| 29 · Nov 7 | Prepare code submission    | Run the tutorial's code-export cell, download `tutorial.zip` or the appropriate required ZIP, and verify that the code is complete.                | Code archive ready                  | 3 h  |
| 30 · Nov 8 | Final audit                | Submit the final candidate and code as required, verify the displayed submission status, back up the notebook, and review all course requirements. | Final submission checklist complete | 3 h  |

The tutorial explicitly states that students aiming for Honors or Outstanding selection must submit their code as well as their prediction submission. Follow the current Omnicampus instructions for the accepted ZIP format.&#x20;

competition_tutorial.pdf



## 4. Daily experiment tracker

Use this table to make sure every experiment teaches you something. The goal is to improve your model systematically instead of trying random changes.

| Experiment | Model / features    | Validation score | Public score | Decision         |
| ---------- | ------------------- | ---------------- | ------------ | ---------------- |
| E00        | Tutorial baseline   | —                | Record       | Benchmark        |
| E01        | Logistic regression | Record           | Record       | Compare          |
| E02        | Random forest       | Record           | Record       | Compare          |
| E03        | Gradient boosting   | Record           | Record       | Compare          |
| E04        | Improved features   | Record           | Record       | Keep or reject   |
| E05        | Tuned finalist      | Record           | Record       | Keep or reject   |
| E06        | Ensemble            | Record           | Record       | Final comparison |

Replace each placeholder with your actual results. Keep the validation split, metric, and experimental conditions consistent when comparing candidates.

## 5. Outstanding Student checklist

## Readiness tracker

### 0/12

### Competition

Run and submit the baseline successfully

Read README.ipynb and column descriptions

Use a consistent local validation method

Test multiple models fairly

Record every experiment and its score

Create a final valid submission.csv

Submit the required code ZIP

### Course performance

Check attendance-survey progress

Check homework points and late-submission rules

Pass the final assignment

Confirm competition participation is recorded

Review overall course-score requirements

&#x20; Copy checklist

## 6. Three rules that will make this plan more effective

1. Protect your course grades. The competition matters, but Outstanding selection also depends on your overall course score. Don't sacrifice homework, surveys, or the final assignment to chase a marginal leaderboard gain.
2. Learn from each experiment. Write down what changed, why you changed it, and whether it improved validation performance.
3. Finish early, submit safely. November 8 is your internal deadline, not the official competition deadline. Keep the remaining time for fixing issues, checking Omnicampus, and making only well-tested improvements.

One final point: your 30-day plan is a structured path toward an Outstanding-level submission, not a guarantee of a top-10% rank. Competition performance depends on your results relative to other students.

Personalize the workload: this plan assumes approximately 3 hours per day, with longer sessions on key experiment days.
