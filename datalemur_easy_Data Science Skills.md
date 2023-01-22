# Data Science Skills

## **Question**

Given a table of candidates and their skills, you're tasked with finding the candidates best suited for an open Data Science job. You want to find candidates who are proficient in Python, Tableau, and PostgreSQL.

Write a query to list the candidates who possess all of the required skills for the job. Sort the output by candidate ID in ascending order.

Assumption:

* There are no duplicates in the candidates table.

>***candidates***  Table:

|Column Name|Type|
|---:|---:|
|candidate_id|integer|
|skill|integer|

>***candidates*** Example Input:

|candidate_id|	skill|
|---:|---:|
123|	Python
123|    Tableau
123|	PostgreSQL
234|	R
234|	PowerBI
234|	SQL Server
345|	Python
345|	Tableau

>**Example Output**:

|candidate_id|
|---:|
|123|

### **Explanation**
Candidate 123 is displayed because they have Python, Tableau, and PostgreSQL skills. 345 isn't included in the output because they're missing one of the required skills: PostgreSQL.

## Solution
---
    SELECT candidate_id 
    FROM candidates 
    WHERE skill IN ('Python', 'Tableau', 'PostgreSQL')
    GROUP BY candidate_id
    HAVING COUNT(skill) = 3
    ORDER BY candidate_id;

Question reference: [datalemur](https://datalemur.com/)
                    Made by Nick Singh, Best-Selling Author of [Ace the Data Science Interview](https://www.amazon.com/dp/0578973839?&linkCode=sl1&tag=datalemur-20&linkId=be42c7443fa05a3c9d783fee4e6f4762&language=en_US&ref_=as_li_ss_tl)

