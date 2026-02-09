# SmartCart - Customer Segmentation Analysis

A data science project that performs customer segmentation using machine learning clustering algorithms to identify distinct customer groups based on purchasing behavior, demographics, and engagement patterns.

## 📊 Project Overview

SmartCart analyzes customer data to segment customers into distinct groups using unsupervised machine learning techniques. This segmentation helps businesses understand their customer base better and tailor marketing strategies accordingly.

## 🎯 Key Features

- **Data Preprocessing**: Handles missing values, outlier detection and removal
- **Feature Engineering**: Creates meaningful features from raw data
  - Customer age calculation
  - Customer tenure (days since joining)
  - Total spending across product categories
  - Total children (kids + teens)
  - Education level simplification
  - Living situation categorization
  
- **Dimensionality Reduction**: Uses PCA to visualize high-dimensional data in 3D space
- **Cluster Analysis**: Implements multiple approaches to determine optimal number of clusters
  - Elbow Method (WCSS)
  - Silhouette Score Analysis
  
- **Clustering Algorithms**:
  - K-Means Clustering
  - Agglomerative Clustering (Hierarchical)
  
- **Visualization**: Comprehensive visual analysis including:
  - Pair plots for feature relationships
  - Correlation heatmaps
  - 3D PCA projections
  - Cluster characterization plots

## 📁 Dataset

**File**: `smartcart_customers.csv`

**Attributes** (2,240 customers):
- **Demographics**: Year of Birth, Education, Marital Status
- **Income**: Annual household income
- **Family**: Number of kids and teens at home
- **Engagement**: Customer join date, recency, website visits, complaints
- **Spending**: Amount spent on wines, fruits, meat, fish, sweets, and gold products
- **Purchases**: Number of deals, web, catalog, and store purchases
- **Campaign Response**: Response to marketing campaigns

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **Scikit-learn** - Machine learning algorithms
  - StandardScaler (data normalization)
  - PCA (dimensionality reduction)
  - KMeans Clustering
  - AgglomerativeClustering
  - OneHotEncoder (categorical encoding)
  - Silhouette Score (cluster validation)
- **KneeLocator** (kneed library) - Optimal k-value detection

## 🚀 Getting Started

### Prerequisites

Install required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn kneed
```

### Running the Analysis

1. Ensure `smartcart_customers.csv` is in the same directory as the notebook
2. Open `SmartCart.ipynb` in Jupyter Notebook or VS Code
3. Run all cells sequentially

## 📈 Analysis Workflow

1. **Data Loading & Exploration**
   - Load customer data
   - Check data shape and missing values

2. **Data Preprocessing**
   - Handle missing income values using median imputation
   - Feature engineering (Age, Customer Tenure, Total Spending, Total Children)
   - Simplify categorical variables (Education, Marital Status)
   - Remove unnecessary columns

3. **Outlier Removal**
   - Remove customers with Age > 90
   - Remove customers with Income > 600,000

4. **Data Encoding & Scaling**
   - One-hot encoding for categorical variables
   - Standard scaling for numerical features

5. **Dimensionality Reduction**
   - Apply PCA to reduce 18 features to 3 principal components
   - Visualize data in 3D space

6. **Optimal Cluster Determination**
   - Elbow Method analysis
   - Silhouette Score calculation
   - **Result**: Optimal k = 4 clusters

7. **Clustering**
   - Apply K-Means clustering
   - Apply Agglomerative clustering
   - Visualize clusters in 3D

8. **Cluster Characterization**
   - Analyze cluster distributions
   - Compare Income vs. Total Spending patterns
   - Generate cluster summary statistics

## 🎯 Results

The analysis identifies **4 distinct customer segments** based on:
- Income levels
- Spending patterns across product categories
- Purchase behavior (web, catalog, store)
- Family demographics
- Educational background
- Customer engagement metrics

Each cluster represents a unique customer persona that can be targeted with specific marketing strategies.

## 📊 Key Insights

- Strong correlation between income and total spending
- Education level and living situation impact purchasing behavior
- Customer tenure influences engagement patterns
- Clear separation of customer segments in 3D PCA space

## 📝 Files in Repository

- `SmartCart.ipynb` - Main analysis notebook with complete workflow
- `smartcart_customers.csv` - Customer dataset (2,240 records)
- `README.md` - Project documentation

## 🔍 Future Enhancements

- Predictive modeling for customer lifetime value
- Campaign response prediction
- Churn analysis and prevention strategies
- Real-time customer segmentation API
- Interactive dashboard for cluster exploration

## 👥 Use Cases

- **Marketing**: Targeted campaign design for each customer segment
- **Product Management**: Understanding product preferences by segment
- **Sales**: Personalized sales approaches based on cluster characteristics
- **Customer Service**: Tailored support strategies for different customer types

## 📧 Contact

For questions or suggestions about this project, please reach out through the repository.

---

**Date**: February 2026  
**Analysis Tool**: Python with Jupyter Notebook
