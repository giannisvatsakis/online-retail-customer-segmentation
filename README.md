# Customer Segmentation: A Clustering Analysis

## 🔗 View Full Analysis

Interactive report with full clustering results, visualizations, and segment interpretation:

[Click here to view the HTML report](outputs/segmentation.html)

---

## Project Overview

This project segments customers of an online retail business using RFM analysis and clustering, with the goal of identifying high-value customers and improving marketing targeting. Using transaction-level retail data, customers are grouped into distinct segments according to how recently they purchased, how often they buy, and how much they spend. High-value customers represent approximately 20% of the customer base but generate the majority of revenue, whereas inactive customers account for a large share of the population with minimal contribution.

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

5. **Log-Transformation**
   - RFM variables were log-transformed to reduce skewness and improve clustering performance

6. **Cluster Selection**
   - Elbow Method
   - Silhouette Analysis

7. **Clustering Algorithms**
   - K-Means clustering
   - Hierarchical clustering

8. **Cluster Evaluation**
   - Silhouette score comparison between clustering methods

---

## Key Insights

- Customer value is highly skewed, with a small segment contributing disproportionately to revenue
- Recency is the strongest differentiator between active and inactive customers
- Frequency and monetary value jointly identify high-value segments more effectively than either alone

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

K-Means clustering produced slightly better cluster separation than hierarchical clustering, as indicated by a higher silhouette score, suggesting more well-defined and compact customer segments.

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

- **Data manipulation:** dplyr, tidyr
- **Visualization:** ggplot2
- **Clustering:** cluster, factoextra

---

## Project Structure

```
online-retail-customer-segmentation/
│
├── data/
│   └── Online Retail.xlsx
│
├── notebooks/
│   └── segmentation.Rmd
│
├── outputs/
│   └── segmentation.html
│
├── README.md
└── .gitignore

```

---

## How to Run

1. Clone the repository
2. Open `notebooks/segmentation.Rmd` in RStudio
3. Install required packages
4. Knit the file to reproduce the analysis

---

## Author

Master's student in **Data Science and Machine Learning - Hellenic Open University**, focusing on statistical analysis, predictive modeling, and business analytics.

---