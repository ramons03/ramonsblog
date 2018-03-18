---
title: SQL update latest entry
tags:
  - SQL
categories: []
date: 2017-08-16 19:06:08
---

Update rows according to an effective date. 

```sql
UPDATE table 
SET activo = 0 
FROM table t1
INNER JOIN 
  (SELECT id,max(fechamodificacion) as LatestDate FROM table
   GROUP BY id) t2 
ON t1.id = t2.id and t1.fechamodificacion < t2.LatestDate
--for last row only use: t1.fechamodificacion = t2.LatestDate
--where
```


