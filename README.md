# Project: Anomaly Detection Using Isolation Forest

## Objective
To detect anomalous customer behavior patterns (e.g., fraud, unusual spend) in an e-commerce dataset using Isolation Forest and derive business insights from the detected outliers.

## Dataset Description (`ecommerce_purchase_data.csv`)
Columns include:
- `CustomerID`: Unique identifier
- `Age`, `Gender`, `AnnualIncome`
- `PurchaseAmount`, `PurchaseFrequency`
- `LastPurchaseDate`: Date of most recent purchase
- `ProductCategory`: Product type bought
- `LoyaltyProgramMember`: 1 if enrolled
- `CustomerRating`: Rating from customer

## Key Steps in Notebook
1. Data exploration and null value treatment
2. Feature engineering:
   - Convert dates to datetime, extract month/year
   - Encode categorical features with OneHotEncoder
3. Train Isolation Forest to detect outliers
   - Parameters: `n_estimators=100`, `contamination=0.05`
   - Outliers tagged using anomaly score threshold
4. PCA used to visualize 2D representation of anomaly vs normal
5. Analyze characteristics of outliers:
   - High income but low purchase behavior
   - One-time buyers
   - Segment patterns by month and product category

## Requirements
- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

To install all dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Folder Structure

<pre><code>
Anomaly-Detection-for-Ecommerce-Purchase-Data
├── data/ # Ecommerce_purchase_data.csv 
├── notebooks/ # Jupyter notebooks for EDA and model training
├── outliers.csv # outliers in a csv file after extracting from the isolation forest
├── Anomaly Detection_Report.pdf # Report consisting of the insight from anomaly detection
└── README.md # Project documentation
</code></pre>

## How to Run
*  Open isolation_forest.ipynb in VS Code (Jupyter) or Jupyter Notebook

*  Place ecommerce_purchase_data.csv in the same folder

*  Run all cells in order to process data, train the model, and view results

## Output
*  Print percentage of detected outliers

* Export outliers.csv with anomaly-labeled records

* PCA plot visualizing anomaly clusters

* Business insights table/markdown section

## Business Use Cases
* Detect high-risk or fraudulent customer behavior

* Identify disengaged or suspicious buying patterns

* Feed insights into retention, loyalty, and fraud-prevention systems
