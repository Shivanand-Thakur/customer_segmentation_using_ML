# 🧩 Customer Segmentation Using K-Means Clustering

This project performs **Customer Segmentation** using **unsupervised machine learning (K-Means)** to group customers based on purchasing behavior, recency, and demographics.  
It provides an **interactive Streamlit dashboard** for deep insights into customer clusters, allowing marketing teams to target high-value segments effectively.

---

## 🚀 **Project Overview**

The goal of this project is to:
- Group customers into distinct clusters based on behavioral and spending data.
- Identify **High-Value**, **Medium**, and **At-Risk** segments.
- Visualize customer clusters and patterns using advanced analytics.
- Deploy a **Streamlit dashboard** for real-time exploration and decision-making.

---

## 🧭 **Stage-Wise Breakdown**

### **Stage 1 — Exploratory Data Analysis (EDA)**
- Cleaned and preprocessed raw marketing campaign data (`marketing_campaign.xlsx`).
- Handled missing values, outliers, and inconsistent data formats.
- Derived new features such as:
  - `Customer_Age`
  - `Tenure_days`
  - `TotalSpend`
- Visualized customer distribution across income, age, recency, and spending categories.
- Tools used: `pandas`, `numpy`, `matplotlib`, `seaborn`.

### **Stage 2 — Model Building and Clustering**
- Implemented **K-Means**, **Agglomerative**, and **Gaussian Mixture Models**.
- Evaluated clustering performance using:
  - Silhouette Score  
  - Calinski-Harabasz Index  
  - Davies-Bouldin Score
- Selected the **best-performing model** (K-Means) and optimized the number of clusters.
- Assigned descriptive labels:
  - `High-Value & Active`
  - `Medium-High Value`
  - `Medium Value`
  - `Low-Value / At-Risk`
- Saved final model and preprocessing artifacts (`imputer`, `scaler`, and trained model) using `joblib`.

### **Stage 3 — Streamlit Deployment**
- Built a fully interactive dashboard using **Streamlit**:
  - 📥 Upload customer data (CSV/XLSX)
  - 🧠 Automatic segmentation into clusters
  - 🔍 Deep dive into each segment
  - 📊 Visual analytics (Cluster Distribution & PCA projection)
  - 📥 Export clustered data as CSV
- Pages included:
  1. **Home** — Upload and summary metrics  
  2. **Deep Segmentation** — Explore spending, recency, and income per cluster  
  3. **Visual Analytics** — PCA visualization and segment distribution  
  4. **Export Results** — Download labeled dataset for marketing use  

---

## 🧰 **Tech Stack**

| Layer | Tools & Libraries |
|-------|-------------------|
| Data Handling | `pandas`, `numpy`, `openpyxl` |
| Visualization | `matplotlib`, `seaborn` |
| Modeling | `scikit-learn`, `joblib` |
| Deployment | `streamlit` |
| Environment | Google Colab (Stages 1–2), VS Code (Stage 3) |

---

## 🧩 **Project Structure**

Customer_Segmentation_Project/
│
├── marketing_campaign.xlsx # Original dataset
├── Requirement document.docx # Requirement brief
│
├── artifacts/
│ ├── stage2_model/
│ │ ├── imputer.joblib
│ │ ├── scaler.joblib
│ │ ├── KMeans_model.joblib
│ │ ├── clustered_data.csv
│ │ ├── cluster_profile_means.csv
│ │ └── cluster_counts.csv
│
├── notebooks/
│ ├── stage1_EDA.ipynb # Data cleaning & visualization
│ └── stage2_Model_Building.ipynb # Model training & evaluation
│
├── streamlit_app.py # Stage 3 Streamlit dashboard
└── README.md # Project documentation

---Create a virtual environment---
python -m venv venv
venv\Scripts\activate    # (Windows)
source venv/bin/activate # (Linux/Mac)

---Install dependencies---
pip install -r requirements.txt

---Run the Streamlit App---
streamlit run streamlit_app.py

