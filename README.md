# Pattern Discovery in Grocery Retail Transactions
**CS 4412: Data Mining | Kennesaw State University**  
**Author:** Freddy Erazo  
**Semester:** Spring 2026

## Project Overview
This repository contains the complete implementation and final documentation for my CS 4412 semester project. The objective was to apply the **Knowledge Discovery in Databases (KDD)** process to a grocery retail dataset to uncover non-obvious patterns in consumer behavior through a combination of association rule mining and unsupervised machine learning.

The project successfully transitions from raw transaction logs to actionable business intelligence, categorizing the retailer as a "daily necessity hub" driven by staple products and a highly loyal VIP shopper segment.

## Key Implementation Features
*   **End-to-End Data Pipeline**: Automated ingestion, cleaning, and transformation of **38,765 transaction records**.
*   **Market Basket Analysis**: Applied the **Apriori Algorithm** to generate 240 rules, identifying high-lift "Product Anchors" such as the Yogurt-Milk relationship (Lift: 2.18).
*   **Customer Segmentation**: Implemented **K-Means Clustering** to segment the shopper base into three distinct behavioral profiles: Occasional, Regular, and VIP shoppers.
*   **Anomaly Detection**: Integrated an **Isolation Forest** algorithm to filter "extreme" shoppers (top 1%), ensuring cluster integrity and protecting against non-human data skew.
*   **Statistical Validation**: Utilized the **Elbow Method** and **Silhouette Analysis** to mathematically verify the optimal cluster count ($k=3$).

## Dataset
*   **Name**: Retail Transaction Dataset (Groceries)
*   **Source**: Kaggle
*   **Scope**: 38,765 records consolidated into **14,963 unique shopping baskets** based on `Member_number` and `Date`.

## Repository Structure
*   `retail_data_project.ipynb`: Primary Jupyter Notebook containing the full pipeline: EDA, Apriori mining, K-Means clustering, and Isolation Forest.
*   `Groceries_dataset.csv`: The raw transaction data.
*   `Analysis_Milestone3.pdf`: A technical report detailing implementation status, analytical choices, and discovery results.
*   `README.md`: Project overview and setup instructions.

## Methodology & Findings

### 1. Preprocessing & Transformation
Data was grouped into "baskets" to represent individual shopping trips. I applied **One-Hot Encoding** for association mining and **StandardScaler** normalization for clustering to ensure the K-Means algorithm treated shopping frequency and volume with equal mathematical weight.

### 2. Mining & Pattern Discovery
*   **Product Anchors**: Identified `{Yogurt} -> {Whole Milk}` as a primary anchor with a **Lift of 2.18**, indicating these items are intentionally sought out together.
*   **Behavioral Segments**:
    *   **Segment 0 (Regulars)**: Routine shoppers averaging 4.4 visits and 11.5 items.
    *   **Segment 1 (Occasional)**: "Top-off" shoppers averaging 2.2 visits and 5.4 items.
    *   **Segment 2 (VIPs)**: High-frequency loyalists averaging 6.9 visits and 18.8 items.

### 3. Business Insights
The analysis suggests a convenience-driven model where items like dairy and produce drive daily traffic. Strategic recommendations include implementing "bundle deals" for high-lift pairs to convert occasional shoppers and developing retention programs for the high-value VIP segment.

## How to Run
1.  **Clone the Repo**:
    ```bash
    git clone [https://github.com/freddyrerazo-ctrl/cs4412-retail-transactions](https://github.com/freddyrerazo-ctrl/cs4412-retail-transactions)
    ```
2.  **Install Dependencies**:
    ```bash
    pip install pandas numpy matplotlib seaborn mlxtend scikit-learn
    ```
3.  **Execute**: Run all cells in `retail_data_project.ipynb` to regenerate the analysis and visualizations.

## Critical Assessment & Future Work
*   **Limitations**: The low support threshold (0.001) used for mining uncovers rare but strong rules; however, these may lack the volume for store-wide physical restructuring.
*   **Future Work**: Integration of temporal stability analysis (day-of-week fluctuations) and the incorporation of demographic data to better understand the "why" behind the VIP segment's behavior.
