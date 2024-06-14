# RFM-Analysis-in-Python
### Why RFM?
- RFM (Recency, Frequency, Monetary) analysis is a marketing model using customer segmentation based on their transaction history.
- This model could be very useful, especially for small and medium-sized enterprises (SMEs) with limited marketing resources, helping them focus on the potentially right customer segments to increase ROI, reduce churn, reduce cost, improve customer relationship, and a lot more.

### How?
- In RFM analysis, customers are scored based on three factors (Recency - how recently, Frequency - how often, Monetary - how much), then labeled based on the combination of RFM scores.

### Reference:
- https://www.putler.com/rfm-analysis

### Introduction
In today’s competitive e-commerce landscape, understanding customer behavior is crucial for devising effective marketing strategies. One powerful method for segmenting customers is the RFM (Recency, Frequency, Monetary) analysis. By evaluating how recently a customer has purchased (Recency), how often they purchase (Frequency), and how much they spend (Monetary), businesses can classify their customers into different segments and tailor their marketing efforts accordingly.
### Data Overview 
This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

The dataset comprises 541,909 entries, detailing transactions from an e-commerce platform.After cleaning the data by removing rows with missing values and filtering out canceled transactions, we retained 406,829 valid records.
 
- **InvoiceNo**: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'C', it indicates a cancellation.
- **StockCode**: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name. Nominal.
- **Quantity**: The quantities of each product (item) per transaction. Numeric.
- **InvoiceDate**: Invoice Date and time. Numeric, the day and time when each transaction was generated.
- **UnitPrice**: Unit price. Numeric, Product price per unit in sterling.
- **CustomerID**: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
- **Country**: Country name. Nominal, the name of the country where each customer resides.
### Building RFM Models
To build the RFM model, we calculated the three key metrics for each customer:

- Recency: The number of days since the customer’s last purchase.
- Frequency: The total number of transactions made by the customer.
- Monetary: The total amount spent by the customer.

We then assigned scores to each metric:

- RecencyScore: Customers were divided into quintiles, with 5 being the most recent purchasers.
- FrequencyScore: Customers were ranked and divided into quintiles, with 5 being the most frequent purchasers.
- MonetaryScore: Customers were divided into quintiles based on their total spending, with 5 being the highest spenders.
- By concatenating these scores, we created a combined RFM score for each customer.

### Visualization 


### Insights and Actionable Strategies
- Focus on Champions: These customers are the most valuable. Personalized offers and exclusive rewards can help in retaining them.
- Nurture Loyal Customers: Encourage repeat purchases through loyalty programs and personalized communication.
- Convert Potential Loyalists: Identify what can make them regular buyers. Targeted promotions and tailored content could be effective.
- Re-engage At Risk Customers: Understand why these customers have not made recent purchases and use win-back campaigns to regain their interest.
- Revive Lost Customers: Special offers or reactivation campaigns might bring them back.
