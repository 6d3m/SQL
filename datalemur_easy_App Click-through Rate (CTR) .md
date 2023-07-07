# App Click-through Rate (CTR) 

## **Question**

Assume you have an events table on app analytics. Write a query to get the app’s click-through rate (CTR %) in 2022. Output the results in percentages rounded to 2 decimal places.

Notes:

- Percentage of click-through rate = 100.0 * Number of clicks / Number of impressions
- To avoid integer division, you should multiply the click-through rate by 100.0, not 100.

>***events***  Table:

Column Name|Type|
---:|---:|
app_id|	integer
event_type|	string
timestamp|	datetime

>***events*** Example Input:

app_id|	event_type|	timestamp
---:|---:|---:|
123|	impression|	07/18/2022 11:36:12
123|	impression|	07/18/2022 11:37:12
123|	click|	07/18/2022 11:37:42
234|	impression|	07/18/2022 14:15:12
234|	click|	07/18/2022 14:16:12


>**Example Output**:

app_id|	ctr
---:|---:
123|	50.00
234|	100.00

## Solution
---
    SELECT 
    app_id,     
    ROUND(100.00 *
        SUM(CASE WHEN event_type='click' THEN 1 ELSE 0 END) / 
        SUM(CASE WHEN event_type='impression' THEN 1 ELSE 0 END),2) AS ctr
    ---
    asd
    ---
    
    FROM events
    WHERE DATE_PART('year',TIMESTAMP) = 2022
    GROUP BY app_id;

    
### **Explanation**

App 123 has a CTR of 50.00% because this app receives 1 click out of the 2 impressions. Hence, it's 1/2 = 50.00%.

Question reference: [datalemur](https://datalemur.com/).
                    Made by Nick Singh, Best-Selling Author of [Ace the Data Science Interview](https://www.amazon.com/dp/0578973839?&linkCode=sl1&tag=datalemur-20&linkId=be42c7443fa05a3c9d783fee4e6f4762&language=en_US&ref_=as_li_ss_tl)
