To only get a few results from a query

## MySQL Syntax
```sql
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
```

## Oracle Syntax
```sql
SELECT column_name(s)
FROM table_name
WHERE ROWNUM <= number;
```
### Example : 
Query the city in STATION with the shortest CITY name   
![Station Table](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)   

**MySQL**
```sql
SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) ASC
LIMIT 1;
```
**Oracle**
```sql
SELECT CITY, LENGTH(CITY) FROM (
  SELECT *
  FROM STATION
  ORDER BY LENGTH(CITY), CITY ASC
)
WHERE ROWNUM = 1;
```
