# Cards Issued Difference

## **Question**

Your team at JPMorgan Chase is soon launching a new credit card, and to gain some context, you are analyzing how many credit cards were issued each month.

Write a query that outputs the name of each credit card and the difference in issued amount between the month with the most cards issued, and the least cards issued. Order the results according to the biggest difference.

>***monthly_cards_issued***  Table:

Column Name|Type|
---:|---:|
issue_month|	integer
issue_year|	integer
card_name|	string
issued_amount|	integer

>***monthly_cards_issued*** Example Input:

card_name|	issued_amount|	issue_month|	issue_year
---:|---:|---:|---:|
Chase Freedom Flex|	55000|	1|	2021
Chase Freedom Flex|	60000|	2|	2021
Chase Freedom Flex|	65000|	3|	2021
Chase Freedom Flex|	70000|	4|	2021
Chase Sapphire Reserve|	170000|	1|	2021
Chase Sapphire Reserve|	175000|	2|	2021
Chase Sapphire Reserve|	180000|	3|	2021

>**Example Output**:

card_name|	difference
---:|---:|
Chase Freedom Flex|	15000
Chase Sapphire Reserve|	10000

## Solution
---
    SELECT 
        card_name,
        -- Calculate the difference in issued amount between the month with the most cards issued, and the least cards issued
        MAX(issued_amount)-MIN(issued_amount) AS difference
    FROM monthly_cards_issued
    GROUP BY card_name
    ORDER BY difference DESC;

    
### **Explanation**

Chase Freedom Flex's best month was 70k cards issued and the worst month was 55k cards, so the difference is 15k cards.

Chase Sapphire Reserve’s best month was 180k cards issued and the worst month was 170k cards, so the difference is 10k cards.

Question reference: [datalemur](https://datalemur.com/).
                    Made by Nick Singh, Best-Selling Author of [Ace the Data Science Interview](https://www.amazon.com/dp/0578973839?&linkCode=sl1&tag=datalemur-20&linkId=be42c7443fa05a3c9d783fee4e6f4762&language=en_US&ref_=as_li_ss_tl)
