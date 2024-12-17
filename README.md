# CryptoClustering

## Overview

In this project, unsupervised machine learning techniques, specifically **K-Means clustering** and **Principal Component Analysis (PCA)**, are applied to analyze cryptocurrency market data. The objective is to determine if 24-hour or 7-day price changes impact the clustering of cryptocurrencies.

The analysis involves:
1. Normalizing and preparing the data.
2. Determining the optimal number of clusters (`k`) using the elbow method.
3. Clustering the data using K-Means.
4. Optimizing the clusters with PCA and comparing results.

---

## Repository Structure  

```  
CryptoClustering/  
│  
├── Crypto_Clustering.ipynb       # Main Jupyter Notebook with the full analysis  
├── Resources/  
│   └── crypto_market_data.csv    # Dataset with cryptocurrency market data  
├── README.md                     # Project documentation  
├── Images/                       # Screenshots and visualizations (optional)  
│  
└── Outputs/                      # Exported results or additional artifacts (optional)  
```  

---

## Objectives  

The project focuses on the following tasks:  

1. **Data Preparation**  
   - Load and explore the dataset.  
   - Normalize the data using `StandardScaler` from scikit-learn.  

2. **Finding Optimal Clusters**  
   - Use the elbow method to identify the optimal value of `k` for K-Means clustering.  

3. **K-Means Clustering**  
   - Apply K-Means to cluster cryptocurrencies based on price change percentages.  
   - Visualize the clusters using scatter plots with `hvPlot`.  

4. **Optimizing with PCA**  
   - Reduce features using **Principal Component Analysis (PCA)**.  
   - Reapply K-Means on the reduced feature set and compare results.  

5. **Analysis and Conclusions**  
   - Evaluate the impact of reducing features using PCA.  

---

## Technologies Used  

- **Python**: Programming language for data analysis and machine learning.  
- **Pandas**: Data manipulation and analysis.  
- **scikit-learn**: For scaling data, K-Means clustering, and PCA.  
- **hvPlot**: Interactive visualizations.  
- **Jupyter Notebook**: For running and documenting the analysis.  

---

## Data Source  

The dataset used is `crypto_market_data.csv`, which contains information on cryptocurrency price changes over 24 hours and 7 days.  

| Column                       | Description                       |  
|------------------------------|-----------------------------------|  
| `coin_id`                    | Cryptocurrency identifier         |  
| `price_change_percentage_24h`| Percentage price change in 24 hrs |  
| `price_change_percentage_7d` | Percentage price change in 7 days |  

---

## Results  

### 1. Data Normalization  

- The data is scaled using `StandardScaler()` to ensure all features are on the same scale.  

### 2. Elbow Method for Optimal Clusters  

Using the elbow method, the optimal value of `k` is determined by plotting the inertia values for cluster sizes ranging from 1 to 11.  

- **Best k for Original Scaled Data**: `k = X` (replace with result).  
- **Best k for PCA Data**: `k = Y` (replace with result).  

### 3. K-Means Clustering  

Clusters were created for both:  
- Original scaled data.  
- PCA-reduced data (3 principal components).  

#### Scatter Plot (Original Data)  
- X-axis: `price_change_percentage_24h`  
- Y-axis: `price_change_percentage_7d`  

#### Scatter Plot (PCA Data)  
- X-axis: `PC1`  
- Y-axis: `PC2`  

### 4. PCA Analysis  

Using PCA, the dimensionality was reduced to **3 principal components**. The explained variance ratio indicates how much variance each component retains:  

- **Total Explained Variance**: `Z%` (replace with result).  

### 5. Comparison of Results  

- Comparing K-Means clustering results before and after PCA demonstrates the impact of dimensionality reduction.  
- Insights include:  
   - Accuracy/consistency of clusters.  
   - Simplification of visualizations.  

---

## Visualizations  

### Elbow Method Plot  
![Elbow Method](Images/elbow_method.png)  

### K-Means Clusters (Original Data)  
![Clusters Original Data](Images/original_clusters.png)  

### K-Means Clusters (PCA Data)  
![Clusters PCA Data](Images/pca_clusters.png)  

---

## Instructions for Running the Project  

1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/your-username/CryptoClustering.git  
   cd CryptoClustering  
   ```  

2. **Install Dependencies**  
   Install required libraries using pip:  
   ```bash  
   pip install pandas scikit-learn hvplot jupyterlab  
   ```  

3. **Run the Jupyter Notebook**  
   Start the Jupyter Lab environment and open `Crypto_Clustering.ipynb`:  
   ```bash  
   jupyter lab  
   ```  

4. **Follow Along**  
   Execute each cell in the notebook to:  
   - Prepare the data.  
   - Run K-Means clustering.  
   - Perform PCA and optimize the clusters.  

---

## Key Questions Answered  

1. **What is the optimal value of k for the original and PCA datasets?**  
2. **How much total variance is explained by the three principal components?**  
3. **What is the impact of using PCA-reduced data for K-Means clustering?**  
