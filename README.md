# DevelopersHub-Data-Science-Internship-Phase-2-Task-2

# Task 2: Customer Segmentation Using Unsupervised Learning

## 📌 Objective
Cluster mall customers based on their spending habits and demographic data, and propose targeted marketing strategies for each identified customer segment.

---

## 📂 Dataset
- **Name:** Mall Customers Dataset
- **Size:** 200 rows × 5 columns
- **Features:**
  - `CustomerID` — Unique customer identifier
  - `Gender` — Male / Female
  - `Age` — Customer age
  - `Annual_Income` — Annual income in k$
  - `Spending_Score` — Score assigned by mall (1–100) based on spending behavior

---

## 🔧 Tools & Libraries
| Library | Purpose |
|---|---|
| `pandas`, `numpy` | Data loading and manipulation |
| `matplotlib`, `seaborn` | Data visualization |
| `scikit-learn` | K-Means clustering, PCA, t-SNE, scaling |

---

## 🚀 My Approach

### 1. Data Loading & Exploration
- Loaded the Mall Customers dataset
- Inspected shape, data types, and missing values (none found)
- Analyzed distributions of Age, Income, and Spending Score

### 2. Exploratory Data Analysis (EDA)
- Plotted histograms for all numeric features
- Visualized gender distribution
- Generated a correlation heatmap and pairplot across numeric features

### 3. Feature Scaling
- Applied `StandardScaler` to normalize Annual Income and Spending Score before clustering
- Scaling ensures no single feature dominates the distance calculations

### 4. Finding Optimal K
Used two methods to determine the best number of clusters:
- **Elbow Method** — plotted inertia vs K (2–10); curve elbows at K=5
- **Silhouette Score** — confirmed K=5 gives the highest score

### 5. K-Means Clustering
- Applied K-Means with K=5 and `n_init=10` for stability
- Assigned cluster labels to each customer

### 6. Dimensionality Reduction & Visualization
- **PCA** — reduced 3 features to 2 principal components for 2D visualization
- **t-SNE** — non-linear dimensionality reduction for better cluster separation view

### 7. Cluster Profiling & Marketing Strategies
- Calculated mean Age, Income, and Spending Score per cluster
- Assigned descriptive segment names and tailored marketing strategies

---

## 📊 Results & Findings

| Cluster | Segment | Avg Income | Avg Score | Strategy |
|---|---|---|---|---|
| 0 | Low Income, Low Spenders | Low | Low | Budget offers, discount coupons, loyalty rewards |
| 1 | High Income, Low Spenders | High | Low | Premium awareness campaigns, personalized offers |
| 2 | Average Income, Average Spenders | Medium | Medium | Upselling, membership programs, referral incentives |
| 3 | Low Income, High Spenders | Low | High | EMI/credit options, budget-friendly premium alternatives |
| 4 | High Income, High Spenders | High | High | VIP membership, luxury products, exclusive early access |

**Key Insights:**
- **5 distinct customer segments** were identified using K-Means clustering
- **High Income, High Spenders (Cluster 4)** are the most valuable customers — priority for VIP and loyalty programs
- **High Income, Low Spenders (Cluster 1)** represent a major untapped opportunity — targeted campaigns could unlock significant revenue
- **Low Income, High Spenders (Cluster 3)** carry financial risk — EMI and budget-friendly options can retain them sustainably
- PCA explained over 80% of variance in just 2 components, confirming strong cluster structure
- t-SNE confirmed well-separated, compact clusters validating the K=5 choice

---
## 👤 Author
**Toufeeq Qader**
Data Science Intern — DevelopersHub Corporation
