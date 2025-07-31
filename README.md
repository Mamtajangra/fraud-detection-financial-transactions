# Fraud Detection in Financial Transactions

This project analyzes a financial transactions dataset to detect fraudulent activities using machine learning techniques.

## Dataset

The original dataset was extremely large (over 6 million rows), so it was split into smaller chunks for easier processing and analysis. The main files used are:

- `fraud_part1.csv`: A chunk of the original dataset containing transaction records.
- `sample_fraud.csv`: A sample subset for quick testing and exploration.

Each record includes features such as:
- `step`: Time step of the transaction
- `type`: Transaction type (PAYMENT, TRANSFER, CASH_OUT, etc.)
- `amount`: Transaction amount
- `nameOrig`: Origin account
- `oldbalanceOrg`, `newbalanceOrig`: Origin account balances before and after transaction
- `nameDest`: Destination account
- `oldbalanceDest`, `newbalanceDest`: Destination account balances before and after transaction
- `isFraud`: Indicates if the transaction is fraudulent
- `isFlaggedFraud`: Indicates if the transaction was flagged as fraud

## Approach

Due to the dataset size, extra operations were performed:
- Data was split into manageable chunks for analysis.
- Preprocessing steps included handling missing values, removing duplicates, and dropping unnecessary columns.
- Machine learning models (e.g., logistic regression) were trained and evaluated on the processed data.

## Results

Results and analysis are documented in [`fraud.ipynb`](fraud.ipynb), including:
- Data exploration and visualization
- Model training and evaluation metrics (accuracy, ROC AUC, classification report)
- Insights on fraud detection performance

## Notes

- The chunking of the dataset allowed for more efficient computation and analysis.
- Some operations and results may differ from those obtained using the full dataset due to the reduced data size.

For more details, see the notebook: [`fraud.ipynb`](fraud.ipynb)# fraud-detection-financial-transactions