# ATS Sales Insights - A Data Analysis Project
#### ATS: A Hardware Company *(not a real company name)* which has differnet stores in different states of India to sell the products. 
- Stores: Surge Store, Nomad Store, Axcel Store, Electrix Store, etc.

- States: Uttar Pradesh, Telangana, Maharashtra, etc.

- Head Office: Delhi

- Sales Director: Ahmad

## Problem Statements
Sales director wants to know in which states ATS is doing good? & accordingly we can offer or give some discount accordingly.

- Q1. Revenue breakdown by cities.

- Q2. Revenue brekdown by years & months.

- Q3. Top 5 customers by revenue & sales quantity.

- Q4. Top 5 products by revenue.

## Approach - Project Planning & Aims Grid
Sales director will call people across all the teams which will be working on this project, like I.T. Team, Data Analysis Team, etc.

### [Aims Grid](https://www.youtube.com/watch?v=6118I9HViuQ)
#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that are not visible before for sales team for decision support & automate them to reduced manual time spent in data gathering.

#### 2. Stake Holders: Who will be involved?
- Sales Director, 
- I.T. Team, 
- Customer Service Team, 
- Data & Analytics Team.

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick & latest sales insights in order to support data driven decision making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with latest data available.
- Sales team able to take better decision & prove 10% cost savings of total spend.
- Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.

#### We have different teams in our organization let's say: 
- IT Team: TedEx
- Data Analysts: Data Avengers
- Data Engineers: Data Miners

### A very simple approach
![alt text](https://raw.githubusercontent.com/ahmadtaquee/Sales_Insights_Tableau/main/flow.jpg)

#### Tutorials: [OLTP & OLAP](https://www.geeksforgeeks.org/difference-between-olap-and-oltp-in-dbms/)

### Instructions to setup MySQL on your Laptop

1. Follow step in this video to install mysql on your local computer
https://www.youtube.com/watch?v=WuBcTJnIuzo

2. SQL database dump is in `part-1.sql` & `part-2.sql` files above. Download files to your local computer and import it.


### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001.

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`


## Dashboards
#### Tableau Public: [Revenue & Profit Analysis](https://public.tableau.com/app/profile/ahmad.taquee7097)

![Revenue](https://raw.githubusercontent.com/ahmadtaquee/Sales_Insights_Tableau/main/Part-1/Dashboard%20-%20Revenue.png)

![Profit Analysis](https://raw.githubusercontent.com/ahmadtaquee/Sales_Insights_Tableau/main/Part-2/Dashboard%20-%20Profit%20Analysis.png)


### Myself
#### LinkedIn: [Click Here](https://www.linkedin.com/in/ahmadtaquee/)

