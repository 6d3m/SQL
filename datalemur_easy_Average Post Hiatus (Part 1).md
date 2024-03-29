# Average Post Hiatus (Part 1)

## **Question**

Given a table of Facebook posts, for each user who posted at least twice in 2021, write a query to find the number of days between each user’s first post of the year and last post of the year in the year 2021. Output the user and number of the days between each user's first and last post.

>***posts***  Table:

Column Name|Type|
---:|---:|
user_id|	integer
post_id|	integer
post_date|	timestamp
post_content|	text


>***posts*** Example Input:

user_id|	post_id|	post_date|	post_content
---:|---:|---:|---:|
151652|	599415|	07/10/2021 12:00:00|	Need a hug
661093|	624356|	07/29/2021 13:00:00|	Bed. Class 8-12. Work 12-3. Gym 3-5 or 6. Then class 6-10. Another day that's gonna fly by. I miss my girlfriend
004239|	784254|	07/04/2021 11:00:00|	Happy 4th of July!
661093|	442560|	07/08/2021 14:00:00|	Just going to cry myself to sleep after watching Marley and Me.
151652|	111766|	07/12/2021 19:00:00|	I'm so done with covid - need travelling ASAP!

>**Example Output**:

user_id|	days_between
---:|---:|
151652|	2
661093|	21

## Solution
---
    SELECT 
        user_id,
        -- Calculate the number of days between last post date and first post date
        EXTRACT(DAY FROM MAX(post_date)-MIN(post_date)::TIMESTAMP) AS days_between 
    FROM posts
    -- Filter the post dates for the year 2021
    WHERE EXTRACT(YEAR FROM post_date:: TIMESTAMP) = 2021
    GROUP BY user_id
    -- Filter the users posted at least twice
    HAVING COUNT(*) > 1
    ORDER BY days_between DESC;


Question reference: [datalemur](https://datalemur.com/).
                    Made by Nick Singh, Best-Selling Author of [Ace the Data Science Interview](https://www.amazon.com/dp/0578973839?&linkCode=sl1&tag=datalemur-20&linkId=be42c7443fa05a3c9d783fee4e6f4762&language=en_US&ref_=as_li_ss_tl)
