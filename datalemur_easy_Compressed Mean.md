# Compressed Mean

## **Question**

You are trying to find the mean number of items bought per order on Alibaba, rounded to 1 decimal place.

However, instead of doing analytics on all Alibaba orders, you have access to a summary table, which describes how many items were in an order (item_count), and the number of orders that had that many items (order_occurrences).

>***items_per_order***  Table:

Column Name|Type|
---:|---:|
item_count|	integer
order_occurrences|	integer


>***items_per_order*** Example Input:

item_count|	order_occurrences
---:|---:|
1|	500
2|	1000
3|	800
4|	1000

There are 500 orders with 1 item in each order; 1000 orders with 2 items in each order; 800 orders with 3 items in each order.

>**Example Output**:

mean|
---:|
2.7|

## Solution
---
    SELECT 
        ROUND(SUM(item_count*order_occurrences)*1.0 / SUM(order_occurrences)*1.0, 1) AS mean 
    FROM items_per_order;

    
### **Explanation**

Let's calculate the arithmetic average:

Total items = (1*500) + (2*1000) + (3*800) + (4*1000) = 8900

Total orders = 500 + 1000 + 800 + 1000 = 3300

Mean = 8900 / 3300 = 2.7

Question reference: [datalemur](https://datalemur.com/).
                    Made by Nick Singh, Best-Selling Author of [Ace the Data Science Interview](https://www.amazon.com/dp/0578973839?&linkCode=sl1&tag=datalemur-20&linkId=be42c7443fa05a3c9d783fee4e6f4762&language=en_US&ref_=as_li_ss_tl)
