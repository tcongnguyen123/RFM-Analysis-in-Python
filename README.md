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
Distribution of RFM Metrics
We began by visualizing the distribution of the three key metrics: Recency, Frequency, and Monetary. This helps in understanding the spread and concentration of these values across the customer base.

![image](https://github.com/tcongnguyen123/RFM-Analysis-in-Python/assets/116703297/b65240a5-548e-4f7f-93f0-8068ee479822)

Customer Count by Segment
We used a treemap to visualize the proportion of customers in each segment. This helps in identifying which segments constitute the largest and smallest parts of the customer base.
![image](https://github.com/tcongnguyen123/RFM-Analysis-in-Python/assets/116703297/7535fa09-bfa3-4e05-9d21-ac643055fb52)

Total Sales by Segment
Next, we visualized the total sales contributed by each segment, highlighting the monetary value each segment brings to the business.
![image](https://github.com/tcongnguyen123/RFM-Analysis-in-Python/assets/116703297/25309e70-14c8-4d27-bf19-9f78acf75a56)

### Definition and recommended action for each customer segment:

| Segment | Characteristics | Recommendation |
| :-: | :-: | :-: |
| Champions | Bought recently, buy often and spend the most! | Reward them. Can be early adopters for new products. Will promote your brand. |
| Loyal | Spend good money with us often. Responsive to promotions. | Upsell higher value products. Ask for reviews. Engage them. |
| Potential Loyalist | Recent customers, but spent a good amount and bought more than once. | Offer membership / loyalty program, recommend other products. |
| New customers | Bought most recently, but not often. | Provide on-boarding support, give them early success, start building relationship. |
| Promising | Recent shoppers, but haven’t spent much. | Create brand awareness, offer free trials |
| Need attention | Above average recency, frequency and monetary values. May not have bought very recently though. | Make limited time offers, Recommend based on past purchases. Reactivate them. |
| About to sleep | Below average recency, frequency and monetary values. Will lose them if not reactivated. | Share valuable resources, recommend popular products / renewals at discount, reconnect with them. |
| At risk | Spent big money and purchased often. But long time ago. Need to bring them back! | Send personalized emails to reconnect, offer renewals, provide helpful resources. |
| Cannot lose them | Made biggest purchases, and often. But haven’t returned for a long time. | Win them back via renewals or newer products, don’t lose them to competition, talk to them. |
| Hibernating customers | Last purchase was long back, low spenders and low number of orders. | Offer other relevant products and special discounts. Recreate brand value. |
| Lost customers | Lowest recency, frequency and monetary scores. | Revive interest with reach out campaign, ignore otherwise. |
