
# LeetCode
Solving Leetcode exercises in SQL.

## Context:
A site to learn to another Way. LeetCode is the platform to help enhance skills, knowledge  technical.
It has lists of exercises in several programming languages ​​and related concepts.
In this project, I will solve the SQL Study Plan with 50 questions from easy to advanced level

🗃️ Site: https://leetcode.com

📁 SQL Questions: https://leetcode.com/studyplan/top-sql-50/

👩🏽‍💻 Ambiente: Workspace at LeetCode.


<div align="center">
 <img src="https://github.com/GabiiKatherin/LeetCodeSQL/assets/71796509/ba717982-2c74-423d-9ea1-82d74138c466" width="70%" alt="Descrição da imagem"><br><br>
 </div>  

# Solved exercises Easy/Medium/Hard:

 1. <b>Recyclable and Low Fat Products:</b> Write a solution to find the ids of products that are both low fat and recyclable.
 >```sql
> SELECT product_id
> FROM Products p
> WHERE low_fats = 'Y'
> AND recyclable = 'Y'
>```

 2. <b>Find Customer Referee</b>: Find the names of the customer that are not referred by the customer with id = 2.
>```sql
>SELECT c.name
>FROM Customer c
>WHERE referee_id != 2 OR referee_id IS NULL
>```

3. <b>Big Countries</b>: Write a solution to find the name, population, and area of the big countries.
>```sql
>SELECT w.name, w.population, w.area
>FROM World w
>WHERE w.area >= 3000000 OR population >= 25000000
>```

4. <b>Article Views I</b>: Write a solution to find all the authors that viewed at least one of their own articles.
>```sql
>SELECT DISTINCT author_id AS id
>FROM Views v
>WHERE author_id = viewer_id
>ORDER BY author_id ASC
>```

5. <b>Invalid Tweets</b>: Write a solution to find the IDs of the invalid tweets. The tweet is invalid if the number of characters used in the content of the tweet is strictly greater than 15.
>```sql
>SELECT tweet_id 
>FROM Tweets t
>WHERE LEN(content) > 15
>```

6. <b>Replace Employee ID With The Unique Identifier</b>: Write a solution to show the unique ID of each user, If a user does not have a unique ID replace just show null.
>```sql
>SELECT empUni.unique_id, emp.name
>FROM Employees emp
>LEFT JOIN EmployeeUNI empUni ON emp.id = empUni.id
>```

7. <b>Product Sales Analysis I</b>: Write a solution to report the product_name, year, and price for each sale_id in the Sales table.
>```sql
>SELECT p.product_name, s.year, s.price
>FROM Sales s
>INNER JOIN Product p ON p.product_id = s.product_id
>```

8. <b>Customer Who Visited but Did Not Make Any Transactions</b>: Write a solution to find the IDs of the users who visited without making any transactions and the number of times they made these types of visits.
>```sql
>SELECT customer_id, COUNT(v.visit_id) AS count_no_trans
>FROM Visits v
>LEFT JOIN Transactions t on t.visit_id = v.visit_id
>WHERE transaction_id IS NULL
>GROUP BY customer_id
>```

9. <b>Rising Temperature</b>: Write a solution to find all dates' Id with higher temperatures compared to its previous dates (yesterday).
>```sql
>SELECT w2.id
>FROM Weather w 
>JOIN Weather w2 ON w.recordDate = DATEADD(day, -1, w2.recordDate)
>WHERE w2.temperature > w.temperature
>```

10. <b>Average Time of Process per Machine</b>: The average time is calculated by the total time to complete every process on the machine divided by the number of processes that were run. The resulting table should have the machine_id along with the average time as processing_time, which should be rounded to 3 decimal places.
> ```sql
> SELECT a.machine_id, ROUND(AVG(a2.timestamp - a.timestamp), 3) AS processing_time
> FROM Activity a
> JOIN Activity a2 ON a.machine_id = a2.machine_id
>                  AND a.process_id = a2.process_id
>                  AND a.timestamp < a2.timestamp
> GROUP BY a.machine_id;
> ```


11.  <b></b>:
12. <b></b>:
13. <b></b>:
14. <b></b>:
15. <b></b>:
16. <b></b>:
17. <b></b>:
18. <b></b>:
19. <b></b>:
20. <b></b>:
21. <b></b>:
22. <b></b>:
23. <b></b>:
24. <b></b>:
25. <b></b>:
26. <b></b>:
27. <b></b>:
28. <b></b>:
29. <b></b>:
30. <b></b>:
31. <b></b>:
32. <b></b>:
33. <b></b>:
34. <b></b>:
35. <b></b>:
36. <b></b>:
37. <b></b>:
38. <b></b>:
39. <b></b>:
40. <b></b>:
41. <b></b>:
42. <b></b>:
43. <b></b>:
44. <b></b>:
45. <b></b>:
46. <b></b>:
47. <b></b>:
48. <b></b>:
49. <b></b>:
50. <b></b>:
