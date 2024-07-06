# SALES-DATA-ANALYSIS
SALES DATA ANALYSIS  PURPOSE:  Analyze sales data to identify trends, top-selling products, and revenue metrics for business decision-making. 
'Row ID',
'Order ID',
'Order Date',
'Order Priority'
'Order Quantity'
'Sales'
'Discount'
'Ship Mode'
'Profit'
'Unit Price'
'Shipping Cost'
'Customer Name'
'Province', 'Region'
'Customer Segment'
'Product Category'
'Product Sub-Category'
'Product Name'
'Product Container'
'Product Base Margin'
'Ship Date'
There are 8399 rows in the dataset.

Technology Used
I have used Pandas for data loading, manipulation and exploration, seaborn and matplotlib for data visualization and sklearn for statistical modeling.

Data Exploration
Checked for missing data All the columns have data for every row except for Product Base Margin column which has 68 missing data points

Find categorical features I am considering the features with less than 50 unique values as categorical data. These are the categorical features in the dataset 'Order Priority', 'Discount', 'Ship Mode', 'Province', 'Region', 'Customer Segment', 'Product Category', 'Product Sub-Category', 'Product Container'.

For each categorical data, I explored the distribution of their values using pie chart. Following insights were gained:
a. Most of the order are from West region followed by Ontario and Prarie b. Majority of the customers are Corporates and Office supplies are the most sold product category. c. Most popular shipping mode is Regular Air with 74% of the orders being shipped by this mode of transport and most of the sold items are packed in small boxes. This is obvious since most of the items sold are office supplies.

The data is available for 4 years 2009 - 2012. 2009 is the most profitable year and 2012 as the least profitable. To analyze why 2012 is the least profitable year, I followed following steps: a. I made bar graph for sales, order quantity, shipping cost and discounts. There was no significant change in these over the years which could indicate a drop in profit for 2012 b. I then plotted the histogram for profits, losses (negative profits) and pie chart of Number of orders sold on Profit vs Number of order sold on Loss each year. It was evident from these that each year number of orders sold on loss are more than number of order sold on profit. But this is valid for all years and did not give me a significant indicator of why profits for 2012 dropped. c. I then plotted profit for each product category for each year. From this I found that for the year 2012, furniture product category suffered significant losses. This is a clear reason why the profits for the year 2012 were much low than other years while other factors like number of sales, orders remained almost the same over the years.

It also found that selling technology products yield most of the profit followed by office supplies and furniture.

The trends for customer segment, Product category sold, Province and region from where the order was made remained consistent over the years.

For the statistical modeling and to gain insights about the profit/loses trends I used a decision tree. a. Positive values were marked 1(Profit), Negative values were marked as 0(Loss) b. 'Order Quantity','Shipping Cost','Product Category', 'Unit Price', 'Sales' featues were used to train the model since these have the most impact on the profit of the order. c. The categorical features were one hot encoded. d. The training data was split into training and validation set Following interesting insights were gained analyzing the decision tree: a) Orders with sales less than 350 mostly lead to loses except furniture or office supplies with cheap shipping cost and comparative higher sales amount. b) It became clear that orders with low sales amount, high shipping cost and low unit price mostly lead to losses. Assuming that shipping cost is incurred by the company it could be a business decision to sell cheap products even if the cost to transport is high so that more customers could try out the products which colud ultimately lead to increase in sales and ultimatley increase in profits. c) For orders above 350 sales, low shipping cost and order quanity more than 10 lead to profits. Also orders with very high sales and high per unit cost are mostly profitable.

Created and Presented by- SURYA B @ Data Analyst LinkedIn ID ( www.linkedin.com/in/suryabs )

Location: India

THE END
