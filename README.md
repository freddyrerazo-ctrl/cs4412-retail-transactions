# Pattern Discovery in Grocery Retail Transactions

## Project Overview

This repository contains my CS 4412: Data Mining semester project. The goal of the project is to perform pattern discovery (not prediction) on a grocery retail transaction dataset. I will analyze shopping baskets to find:

- Frequently co-purchased products using association rule mining (Apriori / FP-Growth).
- Natural customer segments based on purchasing behavior using clustering (e.g., K-Means / Hierarchical).
- Anomalous transactions or customers whose behavior is unusual compared to the majority.

The focus is on understanding patterns in the data and interpreting them, rather than building high-accuracy predictive models.

## Dataset

- **Name:** Retail Transaction Dataset  
- **Source:** Kaggle  
- **Link:** https://www.kaggle.com/datasets/bkcoban/retail-transaction-dataset  

This dataset contains synthetic grocery store transactions, where each row represents a shopping basket with a list of purchased products and related identifiers.

## Project Structure

- `data/`  
  - Intended location for the dataset files (CSV, etc.).  
  - You can add a `.gitignore` here if you want to avoid pushing large raw data files.
- `docs/`  
  - Contains the LaTeX-generated proposal PDF for Milestone M1 (e.g., `M1_proposal.pdf`).
  - Jupyter notebooks for data exploration and experiments.
  - Python scripts for data loading, preprocessing, and analysis.
  - This file, describing the project.

## Planned Techniques

The project will primarily use data mining techniques, including:

- **Association Rules:**  
  Discover frequent itemsets and association rules (support, confidence, lift) from transaction-level baskets to find products commonly purchased together.

- **Clustering:**  
  Build customer-level feature vectors (e.g., average basket size, category preferences) and apply clustering algorithms (K-Means / Hierarchical) to discover customer segments.

- **Anomaly Detection:**  
  Use simple distance-based or rule-based methods to flag transactions or customers whose behavior is significantly different from the majority.


- **Course:** CS 4412 — Data Mining  
- **Institution:** (kennesaw state university)  
- **Semester:** (Spring 2026)  

**Author:**  
- Your Name: Freddy Erazo
