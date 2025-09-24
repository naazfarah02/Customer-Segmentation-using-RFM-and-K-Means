# 📊 Customer Segmentation using RFM, K-Means, and Decision Trees  

## 📌 Executive Summary  
This project applies **RFM (Recency, Frequency, Monetary) analysis** on customer transaction data from a UK-based online retailer. Using **K-Means clustering** and **Decision Tree analysis**, customers were segmented into meaningful groups based on their purchasing patterns. The segmentation enables the business to identify high-value customers, evaluate loyalty, and refine strategies for customer retention and revenue growth.  

The study highlights the power of customer-centric analytics in the e-commerce space and provides a framework for targeted marketing, loyalty programs, and growth strategies.  

## ❓ Business Problem  
In a highly competitive e-commerce environment, online retailers must understand their customer base to answer critical questions:  
- Which customers are the most and least valuable to the business? What are their characteristics? 
- What purchasing patterns exist across products, regions, and time (weekly, monthly, quarterly, yearly)?  

Without structured insights, retailers risk inefficient marketing spend, declining retention, and missed opportunities to increase revenue.  

## 🔬 Methodology  
1. **Data Preprocessing**  
   - Selected relevant variables (Invoice, StockCode, Quantity, Price, Country, InvoiceDate, Customer ID).  
   - Removed nulls, invalid transactions (negative prices/quantities), and filtered for UK customers only.  
   - Created derived variables: **Amount = Quantity × Price**, separated `Date` and `Time`.  
   - Converted fields to appropriate data types and standardized RFM features using **Min-Max scaling**.  

2. **RFM Model**  
   - **Recency (R):** Days since last purchase.  
   - **Frequency (F):** Number of transactions.  
   - **Monetary (M):** Total spend per customer.  
   - Constructed RFM table and quartiles.  

3. **Clustering Analysis**  
   - Applied **log transformation** to reduce skewness in RFM variables.  
   - Used **Elbow Method** to determine optimal clusters (k=3).  
   - Segmented customers into three distinct behavioral clusters.  

4. **Decision Tree Refinement**  
   - Applied decision tree regression on **Cluster 2**, which exhibited the most diverse behavior.  
   - Identified sub-groups within the cluster based on Recency and Frequency splits that strongly influenced Monetary value.  

5. **Interpretation & Recommendations**  
   - Characterized clusters and sub-segments.  
   - Proposed customer-centric strategies tailored to each group.  

## 🛠️ Skills Demonstrated  
- Data Cleaning & Preprocessing (Python, Pandas, Numpy)  
- RFM Analysis  
- K-Means Clustering & Elbow Method  
- Decision Tree Regression  
- Feature Transformation (Log normalization, Scaling)  
- Data Visualization & Interpretation(matplotlib, seaborn)
- Business Analytics & Customer-Centric Strategy  

## 📊 Results  
The analysis identified **three primary customer clusters**:  

- **Cluster 1 – Moderate Shoppers (44.39%)**  
  - Infrequent, low spenders, long recency.  
  - Represent the largest portion of the customer base, steady but low-value.  

- **Cluster 2 – Strong Contributors with Growth Potential (38.75%)**  
  - Occasional buyers with moderate spending.  
  - Show behavioral diversity; decision tree analysis revealed high-potential customers vs. low-engagement outliers.  

- **Cluster 3 – High-Value Loyal Customers (16.86%)**  
  - Recent purchases, frequent buyers, high monetary value.  
  - Smallest group but most impactful for revenue.  

Decision tree sub-segmentation further uncovered **emerging VIPs** and **low-value occasional buyers** within Cluster 2.  

## 💡 Business Recommendations  
1. **High-Value Customers (Cluster 3):**  
   - Prioritize retention with loyalty programs, exclusive offers, and premium experiences.  

2. **Moderate Shoppers (Cluster 1):**  
   - Target with upselling and cross-selling campaigns.  
   - Introduce incentives to increase frequency and average spend.  

3. **Growth-Potential Customers (Cluster 2):**  
   - Use personalized promotions to push mid-tier customers toward VIP status.  
   - Focus campaigns on sub-segments identified by decision tree splits (e.g., high-frequency + recent buyers).  

## 🔮 Next Steps  
- Explore **association analysis** to identify commonly purchased item bundles.  
- Predict **customer lifetime value (CLV)** to strengthen long-term planning.  

---
