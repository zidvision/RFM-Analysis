# RFM Analysis for Online Retail Customers

## Project Objective  
To identify key customer segments based on purchasing behavior using RFM (Recency, Frequency, Monetary) analysis.  
This enables the business to create targeted marketing strategies and improve customer retention for future sales growth.

---

## Dataset Used  
- `Online Retail`  
By: [Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33.](https://archive.ics.uci.edu/dataset/352/online+retail)
---

## Business Questions Answered  
- Who are our most valuable customers?  
- Which customers are at risk of churning?  
- What customer segments can we target with loyalty programs or re-engagement campaigns?  
- How are customers distributed based on their recency, frequency, and spending?

---

## Process  

### Data Cleaning and Transformation 
- Removed null values, duplicates, and canceled orders  
- Converted data types (e.g., date fields) for proper analysis
- Add `Total Price` Column

[View cleaned dataset](https://github.com/zidvision/RFM-Analysis/blob/main/Data/Online_Retail_Cleaned.xlsx)

### RFM Score Calculation  
- **Recency**: Days since last purchase  
- **Frequency**: Total number of transactions  
- **Monetary**: Total money spent  
- Used quantiles to assign R, F, and M scores (1–5) to each customer

[Explore the code](https://github.com/zidvision/RFM-Analysis/blob/main/Code/Customer_Summary_Process.ipynb)

[View Customer Summary](https://github.com/zidvision/RFM-Analysis/blob/main/Data/Customer_Summary.csv)

### Customer Segmentation  
- Combined RFM scores into segments (e.g., Champions, At Risk, Lost, etc.)  
- Segmentation using clustering logic and domain knowledge

[Explore the code](https://github.com/zidvision/RFM-Analysis/blob/main/Code/RFM_Analysis.ipynb)

[View RFM Segment](https://github.com/zidvision/RFM-Analysis/blob/main/Data/RFM_Segmented.csv)

### Dashboard Creation  
Built an interactive dashboard in **Power BI** using the RFM segment data

---

## Dashboard Preview  
Explore the Power BI Dashboard that visualizes:
- RFM and Segment Distribution  
- Customer Segments Breakdown  
- Top Customers  
- Revenue Insights by Segment

👉 [View the interactive dashboard](https://github.com/zidvision/RFM-Analysis/blob/main/Visualization/Dashboard%20Image.png)
👉 [Open Power BI Dashboard](https://github.com/zidvision/RFM-Analysis/blob/main/Visualization/RFM_Dashboard.pbix)

---

## Key Insights  
- The majority of customers are categorized as **Potential Loyalists**, indicating they’ve purchased recently and frequently, but still need nurturing to become top-tier customers.
- **Champions** customers have an average monetary value of over $10,000, with a recency average of 6 days, making them the most valuable and engaged segment.
- Out of 4,331 total customers, 830 (approximately 19%) are classified as **Lost**, meaning they haven’t made a purchase in a long time.

---

## Conclusion  
Using RFM segmentation, we can prioritize our marketing efforts:
- Reward and retain **Champions**  
- Re-engage **At Risk** and **Hibernating** customers with promotions  
- Monitor **New** and **Potential Loyalist** customers to turn them into **Loyal** ones

## Tools
Excel, Python, Jupyter Notebook, Power BI
