Pattern Discovery in Grocery Retail Transactions
CS 4412: Data Mining | Kennesaw State University Author: Freddy Erazo

Semester: Spring 2026

Project Overview
This repository contains my semester project for CS 4412. The objective is to apply the Knowledge Discovery in Databases (KDD) process to a grocery retail dataset to uncover non-obvious patterns in consumer behavior. Unlike traditional predictive modeling, this project focuses on Association Rule Mining to understand product relationships and market basket dynamics.

Key Objectives for Milestone 2:
Exploratory Data Analysis (EDA): Visualizing sales trends, popular items, and customer activity.

Data Preprocessing: Transforming raw transaction logs into grouped "baskets" and performing One-Hot Encoding.

Association Rule Mining: Implementing the Apriori Algorithm to identify high-lift product pairings.

Dataset
Name: Retail Transaction Dataset

Source: Kaggle (Link to Dataset)

Description: The dataset contains 38,000+ rows of grocery transactions. Each record includes a Member ID, Date, and Item Description.

Repository Structure
retail data project.ipynb: The primary Jupyter Notebook containing the end-to-end analysis, EDA plots, and mining results.

Groceries_dataset.csv: The raw transaction data used for analysis.

Summary_Milestone2.pdf: A 2-page report summarizing key insights and technical decisions.

README.md: This file, providing an overview of the project state.

Progress & Methodology (KDD Process)
1. Selection & Preprocessing
To make the data minable, I grouped individual item records by Member_number and Date. This allowed me to reconstruct 14,963 unique shopping baskets. I then applied One-Hot Encoding to convert these categorical lists into a binary matrix suitable for the Apriori algorithm.

2. Exploratory Data Analysis (EDA)
I generated several visualizations to understand the data's distribution, including:

Top 10 most frequent items (identifying "anchor" products).

Distribution of basket sizes (average of 2.6 items per trip).

Sales trends by month and day of the week.

3. Data Mining (Association Rules)
Using the mlxtend library, I applied the Apriori algorithm to discover rules with a Lift > 1. This helped identify specific product "companions"—items that are bought together more often than would be expected by random chance.

How to Run the Project
Clone this repository to your local machine.

Ensure you have Python installed with the following libraries:

pandas

matplotlib

seaborn

mlxtend

Open retail data project.ipynb in Jupyter Notebook or VS Code and run all cells.

Future Work (Milestone 3)
Refining association rules using higher confidence thresholds.

Segmenting rules based on customer loyalty (Heavy Shoppers vs. Occasional Shoppers).

Investigating potential clustering techniques to group similar shopping trips.
