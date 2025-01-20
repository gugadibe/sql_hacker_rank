### Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.

#### The STATION table is described as follows:

![alt text](table.png)

_Query utilizada:_

```sql

WITH city_info AS (
SELECT city,
LENGTH(city) AS city_length
FROM station
),

longest_city AS (
SELECT city,
city_length
FROM city_info
WHERE city_length = (SELECT MAX(city_length) FROM city_info)
ORDER BY city LIMIT 1
),

shortest_city AS (
SELECT city,
city_length FROM city_info
WHERE city_length = (SELECT MIN(city_length) FROM city_info)
ORDER BY city LIMIT 1
)

SELECT * FROM longest_city
UNION ALL
SELECT * FROM shortest_city
```

![alt text](image.png)
