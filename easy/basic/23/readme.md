### Query the total population of all cities in **CITY** where District is **California**.

#### The **CITY** table is described as follows:

![alt text](table.png)

_Query utilizada:_

```sql

SELECT SUM(population) FROM city WHERE district = 'California'

```

![alt text](image.png)
