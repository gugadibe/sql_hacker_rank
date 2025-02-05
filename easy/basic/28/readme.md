### Samantha was tasked with calculating the average monthly salaries for all employees in the **EMPLOYEES** table, but did not realize her keyboard's **0** key was broken until after completing the calculation. She wants your help finding the difference between her miscalculation (using salaries with any zeros removed), and the actual average salary.

#### Write a query calculating the amount of error (i.e.: _actual_ - _miscalculated_ average monthly salaries), and round it up to the next integer.

#### The **EMPLOYEES** table is described as follows:

![alt text](table.png)

_Query utilizada:_

```sql

SELECT CEIL(AVG(salary) - AVG(REPLACE(salary, 0, ""))) AS AVERAGE_SALARY FROM employees

```

![alt text](image.png)
