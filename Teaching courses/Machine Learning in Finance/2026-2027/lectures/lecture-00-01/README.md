# Lecture 0 and Lecture 1

## Course orientation and Python foundations

The presentation introduces the 13-week course structure and then begins the official Week 1 material. The notebook uses both the public Apple price and volume dataset and a real credit-risk dataset from the UCI Machine Learning Repository. It includes additional worked cases so the same Python pattern can be understood across portfolio, market-data and credit-risk questions.

## Assessment reminder

The official weighting is 20% weekly exercises, 40% capstone project, and 40% final examination, with a bonus exercise worth up to 10%.

## Files

- `slides/Lecture_00_01_Course_Orientation_and_Python_Foundations_2026-2027.pptx` — latest presentation with additional worked cases.
- `notebooks/lecture_00_01_colab.ipynb` — runnable Colab notebook.
- The notebook is provided with executed text and plot outputs for study and verification.
- `data/finance-charts-apple.csv` — the stock-market CSV used in the lecture examples.
- `data/credit/default_of_credit_card_clients.csv` — the credit-risk CSV used for the credit-data example.
- `data/data_dictionary.md` — complete variable definitions, target coding, units, provenance, citation, and licence information.
- `exercises/weekly_assignment.md` — the weekly assignment brief.

The Colab and presentation use parallel worked cases: a small portfolio calculation, Apple returns and grouped summaries, credit-risk class balance, borrower segments, and a transparent screening rule. The screening rule is illustrative and is not a validated credit policy.

## Open dataset

Source repository: <https://github.com/plotly/datasets>

Direct CSV: <https://raw.githubusercontent.com/plotly/datasets/master/finance-charts-apple.csv>

The file contains 506 daily observations and 12 columns. The lecture uses the date, Apple closing price, and Apple trading volume columns. The remaining source columns stay in the file so the source data remain intact.

## Credit-risk dataset

Source: <https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients>

Official download: <https://archive.ics.uci.edu/static/public/350/default+of+credit+card+clients.zip>

The included CSV contains 30,000 borrower records, 23 explanatory variables, an identifier, and the target `default payment next month`. The presentation and `data/data_dictionary.md` explain every column, its unit, its coding, and its role in the supervised-learning workflow.

## Running the notebook

Open the notebook in Google Colab and run the cells from top to bottom. The notebook downloads the public CSV directly, so it also runs when opened without cloning the repository. A local copy is included in `data/` for traceability and repository navigation.
