---
title: Recursive Query SQL
tags:
  - SQL
categories: []
date: 2017-07-21 21:21:37
---

```sql
WITH MyTest as
(
  SELECT P.ID, P.Parent_ID, CAST(P.ID AS VarChar(Max)) as Level
  FROM table P
  WHERE P.Parent_ID = 3

  UNION ALL

  SELECT P1.ID, P1.Parent_ID, CAST(P1.ID AS VarChar(Max)) + ', ' + M.Level
  FROM table P1  
  INNER JOIN MyTest M
  ON M.ID = P1.Parent_ID
 )
SELECT * From MyTest
```