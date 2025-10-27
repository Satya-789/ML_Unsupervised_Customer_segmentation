# README - Customer Segmentation Analysis

This repository contains a Jupyter Notebook (`Customer_.ipynb`) detailing the process of segmenting mall customers based on their demographic and spending data using unsupervised machine learning techniques.

---

## 1. Project Goal

The primary objective of this project is to identify distinct groups (segments) of customers within the mall dataset. By understanding these segments, marketing teams can develop **targeted strategies** for promotion, product placement, and personalized customer engagement, ultimately maximizing customer satisfaction and revenue.

---

## 2. Dataset

* **File Name:** `Mall_Customers.csv`
* **Source:** The file is loaded from `/content/sample_data/Mall_Customers.csv` within the notebook environment.
* **Key Features:**
    * `Age`
    * `Annual Income (k$)`
    * `Spending Score (1-100)`
    * `Gender`

---

## 3. Methodology and Key Steps

The analysis follows a standard machine learning workflow for clustering:

1.  **Data Preprocessing and Wrangling:**
    * `CustomerID` column is dropped as it is not needed for clustering.
    * The categorical `Gender` column is converted into a numerical feature (`Is_Male`) using one-hot encoding.
2.  **Feature Engineering:**
    * **`Income_Age_Ratio`**: Annual Income divided by Age (to find wealthy young customers).
    * **`Spending_per_Income`**: Spending Score divided by Annual Income (to find normalized spending habits).
3.  **Feature Scaling:** All relevant features are scaled using **`StandardScaler`** to ensure equal weighting during the clustering process.
4.  **Clustering:**
    * **Algorithm:** **K-Means Clustering** is the primary method used, preceded by **Hierarchical Clustering** (Dendrogram) for preliminary cluster number estimation.
    * **Optimal Clusters (K):** The Elbow Method is employed, and the notebook analysis proceeds with the determination of **5 optimal clusters**.

---

## 4. Technologies and Dependencies

The following Python libraries are required to run the notebook:

* **Data Handling:** `pandas`, `numpy`
* **Clustering:** `sklearn.cluster` (KMeans), `sklearn.preprocessing` (StandardScaler), `scipy.cluster.hierarchy` (sch)
* **Visualization:** `matplotlib.pyplot` (plt), `seaborn` (sns), `plotly.express` (px)

---

## 5. Key Results: The 5 Customer Segments

The clustering analysis resulted in 5 distinct, actionable customer segments:

| Cluster | Key Characteristics | Insight | Recommended Action |
| :--- | :--- | :--- | :--- |
| **1. High-Value Shoppers** | High Income, High Spending | These are the most valuable, loyal customers. | Reward loyalty with exclusive programs, personalized high-end recommendations, and premium services. |
| **2. High-Income/Low-Spending** | High Income, Low Spending | Affluent but cautious; they may shop elsewhere. | Focus on conversion. Offer time-sensitive deals, introduce luxury brands, and remove purchase friction. |
| **3. Enthusiastic Shoppers** | Low Income, High Spending | Impulsive shoppers, high transaction volume, potentially high credit risk. | Focus on frequency and affordability. Promote flash sales, bundled deals, and responsible credit/payment plans. |
| **4. Low-Value Shoppers** | Low Income, Low Spending | Often the youngest demographic, shopping out of necessity, highest potential for future growth. | Focus on growth. Use small introductory incentives (e.g., "$50 off $100"), and build long-term brand affinity. |
| **5. Middle-of-the-Road** | Mid Income, Mid Spending | Stable, reliable, and predictable base. | Maintain engagement with standard seasonal campaigns. Focus on cross-selling to new product categories.
