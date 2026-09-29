# Card Fraud Loss Quantification

Where does card fraud loss concentrate, and what would a simple
flagging rule save, at what cost?

## Findings
*1,852,394 simulated card transactions, Jan 2019 – Dec 2020*

- **5 of 14 merchant categories drove 96% of fraud loss value**
  while representing 38% of transaction volume.
- **A $500+ flagging rule captures $4,233,689 (83%) of fraud loss**,
  at the cost of 17,025 legitimate transactions flagged
  (0.9% of legitimate transactions).

## Data
[Credit Card Transactions Fraud Detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection)
(Kaggle, CC0), simulated with the Sparkov generator. Train and test
files were concatenated; there's no model, so no split was needed.
No missing values. `unix_time` is 7 years off from
`trans_date_trans_time` (a generator error), so all time analysis
uses `trans_date_trans_time`.

## Method
Python (pandas, matplotlib). See `fraud_loss_analysis.ipynb`.