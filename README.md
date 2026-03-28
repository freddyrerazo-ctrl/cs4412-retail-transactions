Pattern Discovery in Grocery Retail Transactions
CS 4412: Data Mining | Kennesaw State University Author: Freddy Erazo

Semester: Spring 2026

Project Overview
This repository contains the complete implementation for my CS 4412 semester project. The objective is to apply the Knowledge Discovery in Databases (KDD) process to a grocery retail dataset to uncover non-obvious patterns in consumer behavior.

While Milestone 2 focused on initial exploration, Milestone 3 brings the project to functional completeness by integrating Market Basket Analysis with Unsupervised Machine Learning (Clustering) to categorize shopper behavior.

Key Implementation Features (Milestone 3 Update)
End-to-End Data Pipeline: Automated ingestion, cleaning, and transformation of 38,000+ transaction records.

Association Rule Mining: Applied the Apriori Algorithm to identify high-lift "Product Anchors" (e.g., the Yogurt-Milk relationship).

Customer Segmentation: Implemented K-Means Clustering to segment the shopper base into three distinct behavioral profiles: Occasional, Regular, and VIP shoppers.

Statistical Validation: Generated a Lift Distribution Analysis to verify the significance of discovered rules.

Dataset
Name: Retail Transaction Dataset (Groceries)

Source: Kaggle

Scope: 38,000+ rows; 14,963 unique shopping baskets reconstructed by Member_number and Date.

Repository Structure
retail data project.ipynb: The primary Jupyter Notebook containing the full pipeline, EDA, Apriori mining, and K-Means clustering.

Groceries_dataset.csv: The raw transaction data.

Analysis_Milestone3.pdf: A 4-page technical report detailing implementation status, analytical choices, and discovery results.

README.md: Project overview and setup instructions.

Methodology & Findings
1. Preprocessing & Transformation
Data was grouped into "baskets" to represent individual shopping trips. I applied One-Hot Encoding for association mining and StandardScaler normalization for clustering to ensure the K-Means algorithm treated shopping frequency and volume with equal mathematical weight.

2. Mining & Pattern Discovery
Product Anchors: Identified {Yogurt} -> {Whole Milk} as a primary anchor with a Lift of 2.18, indicating these items are intentionally sought out together.

Behavioral Segments:

Segment 0 (Occasional): High-volume "top-off" shoppers (1-2 items).

Segment 1 (Regulars): Routine weekly shoppers with consistent hauls.

Segment 2 (VIPs): High-frequency, high-volume loyalists who drive significant revenue.

3. Business Insights
The data suggests a dual-strategy for retail optimization: prioritizing "grab-and-go" efficiency for the majority (Segment 0) while developing loyalty-retention programs for the high-value cluster (Segment 2).

How to Run
Clone the Repo: git clone [Your Repo Link]

Install Dependencies: ```bash
pip install pandas numpy matplotlib seaborn mlxtend scikit-learn

Execute: Run all cells in retail data project.ipynb.

Future Work (Milestone 4)
Temporal Stability Analysis: Investigating if product associations fluctuate based on the day of the week or month.

Visualization Polish: Refining charts to portfolio-quality standards for the final presentation.

Critical Assessment: Evaluating the limitations of the chosen support/confidence thresholds.
