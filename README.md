# Market Basket Analysis using Apriori Algorithm

## Project Overview

This individual university Data Mining project uses Python and the Apriori algorithm to identify frequently purchased grocery items and discover associations between products.

The aim is to explore how transaction data can support retail decisions such as product bundling, promotions, and cross-selling.

## Dataset

- **Source:** [Groceries Dataset — Kaggle](https://www.kaggle.com/datasets/irfanasrullah/groceries)
- **Transactions:** 9,835
- **Unique items:** 169
- **Format:** Each row represents a grocery transaction containing comma-separated items.

## Tools and Libraries

- Python
- Jupyter Notebook / Google Colab
- pandas and NumPy
- mlxtend
- Matplotlib

## Methodology

1. Loaded the grocery transactions from the CSV dataset.
2. Split each transaction into individual purchased items.
3. Converted the transactions into a one-hot encoded matrix using `TransactionEncoder`.
4. Checked for missing values and duplicate basket patterns.
5. Applied Apriori with a minimum support threshold of 0.01.
6. Generated association rules using a minimum confidence threshold of 0.30.
7. Filtered rules with lift greater than 1 and confidence greater than 0.30.
8. Visualized frequent items and the relationship between support and confidence.

Duplicate basket patterns were retained because identical combinations of products may represent separate shopping transactions.

## Key Findings

The most frequently purchased items included:

- Whole milk — approximately 25.55%
- Other vegetables — approximately 19.35%
- Rolls/buns — approximately 18.39%

Association rules were evaluated using support, confidence, and lift to explore potential relationships between grocery products.

These findings can inform retail recommendations, although association rules do not establish that purchasing one product causes another purchase.

## How to Run

1. Download the dataset from the Kaggle source linked above.
2. Save the transaction file as `groceries.csv`.
3. Place it in the same working directory as the Jupyter notebook.
4. Install the required libraries:

```bash
pip install pandas numpy matplotlib mlxtend
```

5. Open the notebook in Jupyter or Google Colab.
6. Run the cells in sequence.

For Google Colab, upload `groceries.csv` into the session before running the data-loading cell.

## Limitations

- Results depend on the selected support and confidence thresholds.
- The analysis identifies product associations rather than causal relationships.
- Findings from this grocery dataset may not generalize to every retail business.
- The project demonstrates exploratory association-rule mining rather than a deployed recommendation system.

## Academic Context

Completed as an individual Data Mining coursework project at Taylor's University in June 2026.

## Dataset Attribution

Groceries Dataset, available on [Kaggle](https://www.kaggle.com/datasets/irfanasrullah/groceries), uploaded by irfanasrullah.

The dataset is not included in this repository pending confirmation of redistribution permissions.
