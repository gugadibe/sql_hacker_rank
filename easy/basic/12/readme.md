### Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.

#### The STATION table is described as follows:

![alt text](table.png)

_Query utilizada:_

```sql

SELECT DISTINCT city FROM station
WHERE RIGHT(city, 1) IN ('a','e','i','o','u');
```

![alt text](image.png)
