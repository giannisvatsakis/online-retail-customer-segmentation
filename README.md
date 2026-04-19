# Customer Segmentation: A Clustering Analysis

## Project Overview

Understanding customer behavior is essential for businesses seeking to improve marketing effectiveness and customer retention. This project applies **RFM analysis and unsupervised machine learning techniques** to segment customers based on their purchasing patterns.

Using transaction-level retail data, customers are grouped into distinct segments according to how recently they purchased, how often they buy, and how much they spend. The resulting segments provide insights that can support targeted marketing strategies and customer engagement initiatives.

---

## Dataset

The analysis uses the **Online Retail dataset** from the UCI Machine Learning Repository. The dataset contains over 500,000 transactions from a UK-based online retailer between December 2010 and December 2011.

Key variables include:

- Invoice number
- Product identifier
- Quantity purchased
- Transaction date
- Unit price
- Customer ID
- Country

The dataset was cleaned to remove cancelled transactions, missing customer identifiers, and invalid purchase records before analysis.

---

## Methodology

The project follows a structured analytical workflow:

1. **Data Cleaning**
   - Removal of missing customer identifiers
   - Exclusion of cancelled transactions
   - Filtering invalid quantities and prices

2. **Feature Engineering (RFM Analysis)**
   - Recency: Days since the last purchase
   - Frequency: Number of transactions per customer
   - Monetary: Total spending per customer

3. **Exploratory Data Analysis**
   - Distribution analysis of RFM variables
   - Correlation analysis

4. **Feature Scaling**
   - Standardization of RFM metrics to ensure comparable distances for clustering algorithms

5. **Cluster Selection**
   - Elbow Method
   - Silhouette Analysis

6. **Clustering Algorithms**
   - K-Means clustering
   - Hierarchical clustering

7. **Cluster Evaluation**
   - Silhouette score comparison between clustering methods

---

## Key Insights

The analysis identified **three distinct customer segments**:

**High Value**
- Recent purchases
- High purchase frequency
- Highest spending levels
- Represent the most valuable customers

**Developing Customers**
- Moderate purchase activity
- Moderate spending
- Potential to become high-value customers with increased engagement

**Inactive-Low Value Customers**
- Long time since last purchase
- Low purchase frequency
- Low overall spending

---

## Model Performance

K-Means clustering produced slightly better cluster separation than hierarchical clustering, with a higher silhouette score.

| Model | Silhouette Score |
|---------|--------|
| K-Means | 0.34 |
| Hierarchical | 0.30 |

---

## Business Implications

The segmentation highlights clear opportunities for targeted customer strategies:

- **Retention strategies** should focus on High Value customers to maintain high-value relationships.
- **Growth strategies** could target Developing customers through promotions and personalized engagement.
- **Reactivation campaigns** may help recover some Inactive-Low value customers and increase overall customer lifetime value.

---

## Tools and Technologies

- **R**
- **readxl**
- **dplyr**
- **tidyr**
- **ggplot2**
- **factoextra**
- **cluster**
- **reshape2**

---

## Project Structure

```
Customer-Segmentation/
│
├── segmentation.Rmd        # Main analysis notebook
├── segmentation.html       # Rendered report
├── README.md               # Project description
└── data/
    └── Online Retail.xlsx  # Dataset
    
```

---

## Author

Master's student in **Data Science and Machine Learning - Hellenic Open University **, focusing on statistical analysis, predictive modeling, and business analytics.

---