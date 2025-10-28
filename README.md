# house-prices-ml-team
Kaggle "House Prices: Advanced Regression Techniques" — Team Project
# 🏠 Kaggle: House Prices - Team Project

This is our team's central to-do list. When you start a task, tell the team!

**Workflow:**
1.  `git pull origin main` (Get the latest code)
2.  `git checkout -b your-name/task-name` (Create your branch)
3.  Do the work for *one* task.
4.  `git add .`, `git commit -m "completed task X"`, `git push origin your-name/task-name`
5.  Create a Pull Request on GitHub.

---

## 🗺️ Phase 1: Exploratory Data Analysis (EDA)

**Goal:** Understand our data.
**Where to work:** `notebooks/01_EDA.ipynb`

* [✅] **Task 1:** Load `train.csv` and `test.csv` into pandas DataFrames.
* [✅] **Task 2:** Print the first 5 rows of the training data (`train_data.head()`).
* [ ] **Task 3:** Get a summary of all columns, their types, and non-null counts (`train_data.info()`).
* [ ] **Task 4:** Get descriptive stats (mean, min, max) for all numeric columns (`train_data.describe()`).
* [ ] **Task 5 (The Big One):** Make a histogram of our target variable, `SalePrice`. (This is the most important column in the project).
* [ ] **Task 6:** Find the 10 columns with the *most* missing values (`.isnull().sum()`).

---


## 🚀 Phase 2: First Baseline Model

**Goal:** Get *any* score on the leaderboard. This helps us know if we're improving.
**Where to work:** `notebooks/02_Baseline_Model.ipynb`

* [ ] **Task 7:** Create a new, simple dataset.
    * Define your features `X` (use *only* `GrLivArea` for now).
    * Define your target `y` (it's `SalePrice`).
* [ ] **Task 8:** Train a simple `LinearRegression` model using `X` and `y`.
* [ ] **Task 9:** Use the trained model to predict on the `test.csv` data. (You'll need to load `test.csv` and grab its `GrLivArea` column).
* [ ] **Task 10:** Create a `submission.csv` file in the correct format (a `SalePrice` column and an `Id` column).
* [ ] **Task 11:** Manually upload the `submission.csv` to Kaggle and log our score!

---

## 🧹 Phase 3: Feature Engineering & Better Model

**Goal:** Clean up the data to build a *smarter* model.
**Where to work:** `notebooks/03_Feature_Engineering.ipynb`

* [ ] **Task 12 (Model):** Re-do the baseline model, but this time use *all* numeric columns (not just `GrLivArea`).
* [ ] **Task 13 (Feature Eng):** Fix missing numeric data. Use `SimpleImputer` from `sklearn` to fill missing numbers with the `mean` or `median`.
* [ ] **Task 14 (Feature Eng):** Create a *new* feature. Make a `TotalSqFt` column by adding `1stFlrSF`, `2ndFlrSF`, and `TotalBsmtSF`.
* [ ] **Task 15 (Model):** Train a `RandomForestRegressor` (it's better than Linear Regression) on your new, clean, numeric dataset.
* [ ] **Task 16 (Submission):** Create a new submission file from the RandomForest model and see if our score improved.