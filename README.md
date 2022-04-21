
# Sales Data Analysi Project 

# Authors

- [@Vishwjeet14](https://github.com/vishwjeet14)


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

# SQL Coomands use in Data Analysis

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

# Dashbord 

Dashboard Link - https://app.powerbi.com/links/zmK6gIm8KC?ctid=e9f22aae-f6f4-40c6-afed-460a4fe1d423&pbi_source=linkShare&bookmarkGuid=af56ec1b-ec12-44b9-bc17-5a29309c56b0

![alt text](https://github.com/vishwjeet14/Atalic-Sales-Data-Analysis-Project/blob/main/Picture/dasboard.png)

# Conclusion

* Total revenue of atalic hardware is 986.56 million INR in four years.
* Total Quantity Sales of diffrent products is 2 Million in four years.
* Most profitable year is 2014 in whic they earn arround 414.31 million INR.
* According to trend least profiatable year is 2020 in which till july they earn 142.24 Million INR.
* Top 5 market according to Revenue is Delhi , Mumbai , Nagpur , Kochi , Ahemdabad.
* Top 5 market according to Quantity of sales is Delhi , Mumbai , Nagpur , Bhopal , Ahemdabad.
* Revenue of atalic hardware is going down over the 4 years.


# Feedback

If you have any feedback, please reach out to us at vishc70@gmail.com

