# Dataset

This folder contains historical daily Bitcoin (BTC-USD) price data used in the project.

- **File:** `BTC-USD-Price-History.csv`
- **Source:** Kaggle (public daily Bitcoin price history dataset)
- **Period:** 2010-08-01 to 2025-01-29
- **Observations:** 5,296 daily rows
- **Columns:** Date, Open, High, Low, Close, Volume

Prices and volume are stored as text with a `$` sign and spaces as thousand separators (for example `$102 680.30`). The notebook converts them to numbers during preprocessing.
