# JOINS
## INNER JOIN
```pgsql
SELECT * FROM a INNER JOIN b ON a.key = b.key
```
![INNER JOIN](img/inner_join.png "inner join")


## LEFT JOIN
```pgsql
SELECT * FROM a LEFT JOIN b ON a.key = b.key
```
![LEFT JOIN](img/left_join.png "left join")


```pgsql
SELECT * FROM a LEFT JOIN b ON a.key = b.key WHERE b.key IS NULL
```
![LEFT JOIN](img/left_join_where_is_null.png "left join where is null")


## RIGHT JOIN
```pgsql
SELECT * FROM a RIGHT JOIN b ON a.key = b.key
```
![RIGHT JOIN](img/right_join.png "right join")


```pgsql
SELECT * FROM a RIGHT JOIN b ON a.key = b.key WHERE a.key IS NULL
```
![RIGHT JOIN](img/right_join_where_is_null.png "right join where is null")

## FULL JOIN
```pgsql
SELECT * FROM a FULL JOIN b ON a.key = b.key
```
![FULL JOIN](img/full_join.png "full join")

```pgsql
SELECT * FROM a FULL JOIN b ON a.key = b.key WHERE a.key IS NULL OR b.key IS NULL
```
![FULL JOIN](img/full_join_where_is_null.png "full join where is null")
