# Cities With Completed Trades

## **Question**

You are given the tables below containing information on Robinhood trades and users. Write a query to list the top three cities that have the most completed trade orders in descending order.

Output the city and number of orders.

>***trades***  Table:

Column Name|Type|
---:|---:|
order_id|	integer
user_id|	integer
price|	decimal
quantity|	integer
status|	string('Completed' ,'Cancelled')
timestamp|	datetime


>***trades*** Example Input:

order_id|	user_id|	price|	quantity|	status| timestamp
---:|---:|---:|---:|---:|---:|
100101|	111|	9.80|	10|	Cancelled|	08/17/2022 12:00:00
100102|	111|	10.00|	10|	Completed|	08/17/2022 12:00:00
100259|	148|	5.10|	35|	Completed|	08/25/2022 12:00:00
100264|	148|	4.80|	40|	Completed|	08/26/2022 12:00:00
100305|	300|	10.00|	15|	Completed|	09/05/2022 12:00:00
100400|	178|    9.90|	15|	Completed|	09/09/2022 12:00:00
100565|	265|	25.60|	5|	Completed|	12/19/2022 12:00:00

>***users*** Table:

Column Name|	Type
---:|---:|
user_id|	integer
city|	string
email|	string
signup_date|	datetime

>***users*** Example Input:

user_id|	city|	email|	signup_date
---:|---:|---:|---:|
111|	San Francisco|	rrok10@gmail.com|	08/03/2021 12:00:00
148|	Boston|	sailor9820@gmail.com|	08/20/2021 12:00:00
178|	San Francisco|	harrypotterfan182@gmail.com|	01/05/2022 12:00:00
265|	Denver|	shadower_@hotmail.com|	02/26/2022 12:00:00
300|	San Francisco|	houstoncowboy1122@hotmail.com|	06/30/2022 12

>**Example Output**:

city|	total_orders
---:|---:|
San Francisco|	3
Boston|	2
Denver|	1

## Solution
---
    SELECT 
    users.city, 
    COUNT(*) as total_orders 
    FROM trades
    JOIN users 
    ON users.user_id = trades.user_id
    WHERE trades.status = 'Completed'
    GROUP BY users.city
    ORDER BY total_orders DESC
    LIMIT 3;
    
### **Explanation**

In this example, San Francisco has first place with 3 orders, Boston has second place with 2 orders, and Denver has third place with 1 order.

Question reference: [datalemur](https://datalemur.com/).
                    Made by Nick Singh, Best-Selling Author of [Ace the Data Science Interview](https://www.amazon.com/dp/0578973839?&linkCode=sl1&tag=datalemur-20&linkId=be42c7443fa05a3c9d783fee4e6f4762&language=en_US&ref_=as_li_ss_tl)
