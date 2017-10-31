title: Extraer numeros de un string
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-10-12 11:59:10
tags:
---
python
```
>>> import re
>>> s = '300 gm'
>>> re.findall('\d+', s)
['300']
>>> s = '300 gm 200 kgm some more stuff a number: 439843'
>>> re.findall('\d+', s)
['300', '200', '439843']
```