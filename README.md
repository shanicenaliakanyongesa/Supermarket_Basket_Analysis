# Supermarket Basket Analysis Project

## Overview

This project performs market basket analysis on retail transaction data to identify patterns in customer purchasing behavior. The analysis focuses on transactions from France and uses the Apriori algorithm to discover frequent itemsets and association rules that can help with product recommendations, store layout optimization, and marketing strategies.

## Project Structure

- `basket.ipynb`: Main Jupyter notebook containing the basket analysis implementation
- `content.ipynb`: Content-based filtering analysis for article recommendations
- `cosine.ipynb`: Cosine similarity calculations for text analysis
- `shared_articles.csv`: Dataset containing article data for content analysis
- `Cosine Similarity.pdf`: Documentation on cosine similarity concepts
- `store.csv`: Retail transaction dataset (not included in repository)
- `README.md`: This documentation file
- `TODO.md`: Project task tracking

## Basket Analysis Methodology

### Data Preparation
1. Load retail transaction data
2. Filter transactions to focus on France
3. Create a transaction-item matrix using pivot tables
4. Convert quantities to binary format (purchased/not purchased)

### Frequent Itemset Mining
- Apply Apriori algorithm with minimum support threshold (7%)
- Identify item combinations that appear frequently together

### Association Rule Generation
- Generate rules from frequent itemsets using lift metric
- Filter rules based on lift (>5) and confidence (>0.7) thresholds

### Key Metrics
- **Support**: Frequency of itemset occurrence
- **Confidence**: Likelihood of consequent given antecedent
- **Lift**: Strength of association beyond random chance

## Setup Instructions

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Required packages: pandas, matplotlib, mlxtend

### Installation

1. Clone or download the project files
2. Install required dependencies:
   ```bash
   pip install pandas matplotlib mlxtend
   ```

3. Place the `store.csv` dataset in the project directory
4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

5. Open `basket.ipynb` and run the cells sequentially

## Dataset Description

The analysis uses a retail transaction dataset with the following columns:
- InvoiceNo: Unique transaction identifier
- Description: Product description
- Quantity: Number of items purchased
- Country: Country of transaction

## Analysis Results

### Key Findings
- Identified frequent item combinations in French transactions
- Discovered strong association rules with high lift and confidence


## Dependencies

- pandas: Data manipulation and analysis
- matplotlib: Data visualization
- mlxtend: Machine learning extensions (Apriori algorithm)

