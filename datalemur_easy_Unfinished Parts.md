# Page With No Likes

## **Question**

Tesla is investigating bottlenecks in their production, and they need your help to extract the relevant data. Write a query that determines which parts have begun the assembly process but are not yet finished.

Assumptions

- Table parts_assembly contains all parts in production.
- A part with no finish_date is an unfinished part.

>***parts_assembly***  Table:

|Column Name|Type|
|---:|---:|
part|	string
finish_date|	datetime
assembly_step|	integer

>***parts_assembly*** Example Input:

|page_id|	page_name|
|---:|---:|
20001|	SQL Solutions
20045|    Brain Exercises
20701|	Tips for Data Analysts

>**Example Output**:

|part|
|---:|
|bumper|

### **Explanation**
The only item in the output is "bumper" because step 3 didn't have a finish date.

## Solution
---
    SELECT DISTINCT part 
    FROM parts_assembly
    WHERE finish_date IS NULL;



