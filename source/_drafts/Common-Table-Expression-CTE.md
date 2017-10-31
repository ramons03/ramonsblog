title: Common Table Expression (CTE)
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-21 21:19:05
tags:
---
##What is a Common Table Expression (CTE)

A CTE can be thought of as a temporary result set and are similar to a derived table in that it is not stored as an object and lasts only for the duration of the query. A CTE is generally considered to be more readable than a derived table and does not require the extra effort of declaring a Temp Table while providing the same benefits to the user. However; a CTE is more powerful than a derived table as it can also be self-referencing, or even referenced multiple times in the same query.  

```sql
--The basic syntax structure for a CTE is shown below:
WITH MyCTE
AS ( SELECT EmpID, FirstName, LastName, ManagerID
FROM Employee
WHERE ManagerID IS NULL )
SELECT *
FROM MyCTE
```