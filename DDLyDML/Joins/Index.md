# JOINS
## INNER JOIN
```pgsql
SELECT * FROM a INNER JOIN b ON a.key = b.key
```

## LEFT JOIN
```pgsql
SELECT * FROM a LEFT JOIN b ON a.key = b.key
```

```pgsql
SELECT * FROM a LEFT JOIN b ON a.key = b.key WHERE b.key IS NULL
```

## RIGHT JOIN
```pgsql
SELECT * FROM a RIGHT JOIN b ON a.key = b.key
```

```pgsql
SELECT * FROM a RIGHT JOIN b ON a.key = b.key WHERE a.key IS NULL
```

## FULL JOIN
```pgsql
SELECT * FROM a FULL JOIN b ON a.key = b.key
```

```pgsql
SELECT * FROM a FULL JOIN b ON a.key = b.key WHERE a.key IS NULL OR b.key IS NULL
```
