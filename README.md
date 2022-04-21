
# Sales Data Analysi Project 


In this project I am doing sales analysis of atalic hardwares.For Data analysis i use Power BI and SQL as a tool. Data is collected from the local Database Mysql.  In sales Database there are five tables present.

* Customer
* Date 
* Market
* Production
* Market

These tables are related each other with primary and foreign keys.


# Data Analysis tools

![Logo](https://www.pei.com/wp-content/uploads/2016/08/maxresdefaultreduced.jpg)
![Logo](https://download.logo.wine/logo/MySQL/MySQL-Logo.wine.png)

## Data Analysis Using SQL

* **Show all customer records**

SELECT * FROM sales.customers;

* **Show total number of customers**

SELECT count(*) FROM sales.customers;

* **Show transactions for Chennai market (market code for chennai is Mark001)**

SELECT * FROM sales.transactions where market_code='Mark001';

* **Show distrinct product codes that were sold in chennai**

SELECT distinct product_code FROM sales.transactions where market_code='Mark001';

* **Show transactions where currency is US dollars**

SELECT * from sales.transactions where currency="USD"

* **Show transactions in 2020 join by date table**

SELECT sales.transactions.*, sales.date.* FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020;

* **Show total revenue in year 2020**

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020;

* **Show total revenue in year 2020 in Chennai**

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.transactions.market_code="Mark001";
## Demo

Demo Link - https://app.powerbi.com/links/zmK6gIm8KC?ctid=e9f22aae-f6f4-40c6-afed-460a4fe1d423&pbi_source=linkShare&bookmarkGuid=af56ec1b-ec12-44b9-bc17-5a29309c56b0
## Authors

- [@Vishwjeet14](https://github.com/vishwjeet14)


## Feedback

If you have any feedback, please reach out to us at vishc70@gmail.com

