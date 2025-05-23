# MSCS_634_Lab_1: Data Visualization, Preprocessing, and Statistical Analysis

## Purpose of the Lab Work

The objective of this lab was to systematically explore and analyze a real-world auto sales dataset by applying essential data science methods. This included importing and cleaning the data, identifying and addressing missing values and outliers, reducing data complexity, normalizing features, and performing comprehensive statistical analyses. Through visualizations and quantitative measures, the lab aimed to extract meaningful business insights, demonstrate the relationships between key variables, and practice foundational data preprocessing and analysis skills essential for future advanced modeling and decision-making.

## Key Insights from Visualizations and Statistical Measures

- **Relationship Between Quantity Ordered and Sales:**  
  The scatter plot and correlation matrix indicated a moderate positive correlation (approximately 0.55) between quantity ordered and sales revenue. This confirms that higher order quantities tend to result in greater sales, but also suggests that sales are influenced by other variables such as price and deal size. Businesses should leverage this insight to encourage bulk purchases while considering pricing strategies.

- **Sales Trends Over Time:**  
  The line plot tracking total sales over time revealed fluctuating sales volumes with pronounced peaks in late 2018 and 2019, likely corresponding to seasonal demand surges or marketing initiatives. Although sales varied significantly, no clear upward or downward trend was observed over the period, implying steady but cyclical market behavior that companies can plan around.

- **Product Line Popularity:**  
  The bar chart demonstrated that ‘Classic Cars’ had the highest number of orders, followed by ‘Vintage Cars’ and ‘Motorcycles.’ This distribution highlights key product segments driving revenue. Prioritizing inventory and promotional efforts toward these lines could maximize sales efficiency and customer satisfaction.

- **Sales Distribution:**  
  The sales histogram showed a right-skewed distribution with sales ranging from approximately $482 to $7,947, an average sale of about $3,381, and a median of $3,139. The interquartile range (IQR) of 2,164 suggests notable variability. Most transactions fall into moderate sales amounts, but a few high-value sales significantly affect total revenue. This distribution indicates the need to balance marketing and operational focus on both frequent moderate sales and less frequent but impactful large sales.

- **Sales by Deal Size:**  
  Box plot analysis indicated that ‘Large’ deals typically correspond with higher sales figures and exhibited greater variability, including significant outliers that represent exceptional transactions. In contrast, ‘Medium’ and ‘Small’ deals had lower median sales with more consistent values. This suggests a tiered sales strategy could be effective, tailoring efforts according to deal size characteristics.

- **Order Proportions by Deal Size:**  
  The pie chart revealed that approximately 50% of orders are ‘Medium’ size, closely followed by ‘Small’ deals, while ‘Large’ deals comprise only about 5.5% of transactions. This distribution implies most customers purchase in small to moderate quantities, which can guide resource allocation and sales targeting strategies.

- **Statistical Measures Summary:**  
  Detailed descriptive statistics showed the minimum sales value at $482.13 and a maximum at $7,947.31, with a mean of $3,381.09 and median near $3,139. The standard deviation of 1,575.71 reflects high sales variability. Correlation analysis underscored strong positive correlations between sales and price each (0.79), sales and MSRP (0.63), and a moderate correlation between sales and quantity ordered (0.55). Negative correlations between days since last order and sales (-0.31) indicate that more recent customers tend to have higher purchase amounts.

## Challenges Faced and Decisions Made

- **Missing Data:**  
  The dataset contained no missing values, which simplified preprocessing and ensured completeness. However, checks were rigorously performed across all columns to verify this and guarantee the reliability of the data for subsequent analysis.

- **Outlier Detection and Removal:**  
  Outliers in the sales variable were detected using the Interquartile Range (IQR) method and removed to reduce distortion of statistical measures and improve model robustness. This helped focus analysis on typical transactions while acknowledging outliers as important but exceptional cases.

- **Scaling Without External Libraries:**  
  Because the `scikit-learn` library was not available, Min-Max scaling was implemented manually using pandas and numpy. This workaround successfully normalized key numeric features, ensuring consistent scales across variables for analysis.

- **Feature Selection and Data Reduction:**  
  To maintain privacy and analytical focus, columns containing customer personally identifiable information such as names, phone numbers, and addresses were dropped. Additionally, random sampling reduced the dataset size, improving computational efficiency without significantly impacting analytical insights.

- **Date Conversion:**  
  Converting the ‘ORDERDATE’ column from string to datetime format was critical for accurate chronological grouping and time series visualization. This step enabled meaningful analysis of sales trends and seasonality over the dataset’s timespan.

- **Discretization:**  
  The continuous ‘DAYS_SINCE_LASTORDER’ variable was discretized into three bins labeled ‘Recent’, ‘Moderate’, and ‘Old’. This transformation allowed easier segmentation of customers based on recency, facilitating targeted marketing and retention strategies.

- **Visualization Choices and Interpretation:**  
  Each visualization type was deliberately chosen to best represent the underlying data characteristics and relationships. Careful interpretation of these charts provided actionable insights and clear communication of complex data patterns, supporting informed business decisions.

In conclusion, this lab reinforced practical skills in data preprocessing, visualization, and statistical analysis using a real dataset. It illustrated the importance of data quality, thoughtful feature engineering, and appropriate visual tools to uncover insights that can drive business strategy and future data science work.
