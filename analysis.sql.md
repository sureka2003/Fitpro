

**Retrieve the name and membership\_type of female members.**

```sql
select  m.name,ms.membership\_type  
from memberships as ms  
join members as m on ms.member\_id \= m.member\_id  
where ms.gender \= 'F';

```
**Find members who have a Monthly membership and joined after 2023-11-01.**

```sql
select member\_id,age,gender  
from memberships  
where membership\_type \= 'Monthly'  
and join\_date \> '2023-11-01';
```
 **List the name and status of active members over 25\.**

```sql
select m.name,ms.status  
from memberships as ms  
join members as m on m.member\_id \= ms.member\_id  
where status \= 'Active'  
and age \> 25;

```
**Get details of visits on a specific date (2024-01-01).**

```sql
select \*  
from visits  
where visit\_date \= '2024-01-01';
```

**List members with a Quarterly membership aged between 20 and 30\.**

```sql
select ms.member\_id,m.name, ms.age,ms.gender  
from memberships as ms  
join members as m on m.member\_id \= ms.member\_id  
where ms.membership\_type \= 'Quarterly'  
and ms.age between 20 AND 30;
```

**ADDITIONAL AGGREGATIONS AND GROUPING:** 

**Count the total visits made by each member.**

```sql
select member\_id,  
count (member\_id) as no\_of\_visits  
from visits  
group by member\_id  
Order by no\_of\_visits DESC;
```

**Count of members by membership type** 

```sql
select membership\_type,  
count(member\_id)  
from memberships  
group by membership\_type;
```

**Calculate the average age of members. Grouped by membership type**

```sql
select membership\_type,   
avg(age) as avg\_age  
from memberships  
group by membership\_type  
order by avg\_age ASC;
```

**Calculate total visits of each visit date**

```sql
select visit\_date,   
count(visit\_id)  
from visits  
group by visit\_date;
```

**Count members by status**

```sql
select status,   
count(member\_id)  
from memberships  
group by status;
```


**ADVANCED QUERIES:**

**Identify the top 3 members with the highest visits.**

```sql
SELECT member\_id,   
       COUNT(visit\_id) AS visit\_count  
FROM Visits  
GROUP BY member\_id  
ORDER BY visit\_count DESC  
LIMIT 3;
```
**List active monthly members grouped by membership type,sorted by top 2 join dates.**

```sql
select membership\_type,  
count(member\_id)  
from memberships  
where membership\_type \= 'Monthly'  
AND  
      Status \= 'Active'  
group by membership\_type  
Order by max(Join\_date) DESC  
Limit 2 ;
```

**Retrieve members with more than 2 visits,sorted by total visits,displaying the top 5\.**

```sql
select member\_id,   
count(visit\_id) as total\_visits  
from visits  
group by member\_id  
Having count(visit\_id) \> 2  
order by total\_visits DESC  
Limit 5;
```
**Identify members joined in 2023, grouped by membership type (with each group having more than 1 member).**

```sql
select membership\_type,   
count(member\_id) as total\_no\_of\_members,  
extract(year from join\_date) as join\_year  
from memberships  
where extract(year from join\_date) \= 2023   
group by membership\_type,join\_year  
Having count(member\_id)\>1;
```

**Find the average age of members who have Active membership status, grouped by membership\_type, ordered by membership\_type alphabetically, and limit them  to 3\.**

```sql
select membership\_type,  
avg(age)  
from memberships  
where status \= 'Active'  
group by membership\_type  
order by membership\_type ASC  
Limit 3;  
```
