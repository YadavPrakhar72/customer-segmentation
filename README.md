# Customer Segmentation using K-Means Clustering

### An unsupervised machine learning project to group customers based on their annual income and spending behavior, identifying 5 distinct segments for targeted marketing.

---

## 1. Problem Statement & Goal 🎯

For a business like a shopping mall, understanding the customer base is crucial for creating effective marketing strategies. A one-size-fits-all approach is often inefficient. This project aims to solve this problem by applying unsupervised machine learning to segment customers into distinct groups based on their purchasing patterns.

The primary goal is to identify meaningful customer segments from the `Mall_Customers` dataset, which can help the business tailor its marketing efforts and improve customer satisfaction.

---

## 2. Tech Stack 🛠️

* **Language:** Python
* **Libraries:**
    * Pandas
    * NumPy
    * Matplotlib
    * Seaborn
    * Scikit-learn

---

## 3. The Dataset

* **Source:** The project uses the `Mall_Customers.csv` dataset. This dataset contains information about customers in a mall.
* **Description:** The dataset has 200 entries and 5 columns:
    * `CustomerID`: A unique identifier for each customer.
    * `Gender`: The gender of the customer.
    * `Age`: The age of the customer.
    * `Annual Income (k$)`: The annual income of the customer in thousands of dollars.
    * `Spending Score (1-100)`: A score assigned by the mall based on customer behavior and spending nature.
* **Data Cleaning:** A check for missing values was performed, and the dataset was found to be clean with no null entries.

---

## 4. Workflow & Key Findings 📊

The analysis focused on segmenting customers based on two key features: `Annual Income` and `Spending Score`.

1.  **Finding the Optimal Number of Clusters:**
    * The **Elbow Method** was used to determine the optimal number of clusters for K-Means.
    * By calculating the Within-Cluster Sum of Squares (WCSS) for a range of cluster numbers (1 to 10), the "elbow point" on the graph was identified at **k=5**. This indicates that 5 is the optimal number of clusters.

2.  **Modeling:**
    * A K-Means clustering model was trained with `n_clusters=5`.
    * Each data point (customer) was assigned to one of the 5 clusters based on its features.

3.  **Results & Visualization:**
    * The model successfully grouped the customers into 5 distinct segments, which were visualized using a scatter plot. The clusters can be interpreted as:
        * High Income, Low Spending Score
        * High Income, High Spending Score (Target Customers)
        * Medium Income, Medium Spending Score
        * Low Income, Low Spending Score
        * Low Income, High Spending Score

---
