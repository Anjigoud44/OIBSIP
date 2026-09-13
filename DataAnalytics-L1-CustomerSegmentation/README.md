# Customer Segmentation Analysis

**OASIS Infobyte Internship - Data Analytics Track (Level 1, Task 2)**

## 🎯 Project Objective
The goal of this project is to apply clustering algorithms to segment an e-commerce company's customer base into distinct groups based on purchasing behavior. This segmentation enables the business to implement targeted, highly effective marketing strategies.

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** pandas, scikit-learn, matplotlib, seaborn
* **Environment:** Jupyter Notebook / Google Colab

## 📊 Dataset
This project utilizes the **Online Retail** dataset from the UCI Machine Learning Repository. It contains 541,909 transactions from a UK-based online retailer, capturing customer purchasing data over a one-year period.

## ⚙️ Project Workflow
1. **Data Cleaning:** Removed missing `CustomerID` rows, filtered out canceled orders, and eliminated negative quantities/prices.
2. **Feature Engineering (RFM):** Calculated Recency (days since last purchase), Frequency (total number of purchases), and Monetary (total spend) for each customer.
3. **Standardization:** Scaled the RFM features using `StandardScaler` to ensure equal weighting for the clustering algorithm.
4. **Optimal K Selection:** Utilized the Elbow Method to determine the ideal number of clusters (K=4).
5. **K-Means Clustering:** Applied the K-Means algorithm to assign every customer to a distinct behavioral segment.
6. **Visualization & Profiling:** Generated scatter plots to visualize the clusters and calculated mean feature values to profile each segment.

## 💡 Customer Segments & Marketing Recommendations
Based on the K-Means clustering, the customer base was divided into four distinct profiles:

*   **The Champions (High Frequency, High Monetary, Low Recency):** 
    *   *Profile:* Your most valuable and loyal customers.
    *   *Action:* Reward them with loyalty programs, early access to new product launches, and personalized VIP experiences to maintain their brand advocacy.
*   **Recent & Promising (Low Recency, Low Frequency/Monetary):** 
    *   *Profile:* Customers who recently made their first few purchases.
    *   *Action:* Build the relationship through welcome emails, onboarding guides, and small discounts on their next purchase to encourage repeat buying.
*   **At Risk (High Recency, Average Frequency/Monetary):** 
    *   *Profile:* Customers who used to buy often but have not visited in a while.
    *   *Action:* Deploy targeted win-back campaigns using personalized "We miss you" emails with time-limited discounts to incentivize a return visit.
*   **Lost / Hibernating (Very High Recency, Low Frequency/Monetary):** 
    *   *Profile:* Customers who made a small purchase a long time ago and never returned.
    *   *Action:* Keep them on standard promotional email lists, but allocate primary acquisition and retention budgets toward higher-value segments.

## 📁 Repository Structure
* `Customer_Segmentation_Analysis.ipynb`: The complete Python source code containing data cleaning, modeling, and visualizations.
* `Online_Retail.xlsx`: The dataset used for the analysis (or a link to the UCI repository).
* `README.md`: This project documentation file.

## 🎥 Video Demonstration
[Insert link to your LinkedIn demo video here]
