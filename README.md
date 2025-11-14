# README - Customer Segmentation Analysis using Unsupervised Machine Learning

This repository contains a Jupyter Notebook (Customer_.ipynb) demonstrating a complete customer segmentation workflow using clustering techniques. The analysis focuses on uncovering hidden customer groups within a mall dataset to support targeted marketing and data-driven business decisions.

📌 1. Project Objective

The goal of this project is to identify meaningful customer segments based on demographics and spending behavior. These insights help businesses:

Tailor marketing campaigns

Personalize recommendations

Improve retention and engagement

Support store layout and inventory decisions

Maximize revenue through targeted segmentation

📊 2. Dataset Overview

File: Mall_Customers.csv
Loaded From: /content/sample_data/Mall_Customers.csv

Dataset Features

CustomerID (dropped during preprocessing)

Gender

Age

Annual Income (k$)

Spending Score (1–100)

This is a widely used dataset for practicing clustering and market segmentation.

🔧 3. Workflow & Methodology

The notebook follows a structured machine learning pipeline:

A. Data Preprocessing

Dropped CustomerID

Converted Gender into a numerical flag (Is_Male) using one-hot encoding

Verified dataset completeness (no missing values)

B. Feature Engineering

Additional features extracted for richer segmentation:

Income_Age_Ratio

Highlights younger high-income customers

Spending_per_Income

Normalizes spending relative to income

C. Feature Scaling

All numerical features standardized using StandardScaler to ensure equal impact during clustering.

D. Clustering Techniques

Two clustering strategies applied:

1. Hierarchical Clustering

Dendrogram used to estimate cluster range

2. K-Means Clustering (Primary Method)

Elbow Method used to determine optimal K

Final model trained using K = 5 clusters

📦 4. Technologies & Dependencies

The project uses the following Python libraries:

pandas
numpy
matplotlib
seaborn
plotly
scipy
scikit-learn

🧩 5. Results — The 5 Customer Segments
Cluster	Characteristics	Insight	Recommended Action
1. High-Value Shoppers	High Income, High Spending	Loyal and highly profitable	Provide premium loyalty perks, exclusives
2. High Income / Low Spending	High income, cautious spenders	Potential lost revenue	Promote luxury products, reduce purchase friction
3. Enthusiastic Shoppers	Low income, high spending	Impulsive, high transaction volume	Use bundle deals, flash sales, responsible financing
4. Low-Value Shoppers	Low income, low spending	Young customers with growth potential	Offer small discounts, long-term retention strategies
5. Middle-of-the-Road	Mid income and spending	Stable and consistent base	Use regular seasonal promotions, cross-sell new categories
