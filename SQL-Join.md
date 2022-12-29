# Different types of joins in SQL

## INNER JOIN
```SQL
SELECT *
FROM orders
INNER JOIN customers
ON orders.customer_id = customers.id
```

An inner join returns only rows that match the join condition in both tables. In this case, the `orders` table is joined with the `customers` table using the `customer_id` column from the `orders` table and the `id` column from the `customers` table.

## OUTER JOIN

### LEFT JOIN
```SQL
SELECT *
FROM orders
LEFT JOIN customers
ON orders.customer_id = customers.id
```


A left join returns all rows from the left table (`orders` in this case), and any matching rows from the right table (`customers`). If there is no match in the right table, the columns from the right table will be filled with NULL values.

### RIGHT JOIN

```SQL
SELECT *
FROM orders
RIGHT JOIN customers
ON orders.customer_id = customers.id
```

A right join is similar to a left join, but it returns all rows from the right table (`customers`) and any matching rows from the left table (`orders`). If there is no match in the left table, the columns from the left table will be filled with NULL values.

### FULL OUTER JOIN

```SQL
SELECT *
FROM orders
FULL OUTER JOIN customers
ON orders.customer_id = customers.id
```


A full outer join returns all rows from both tables, regardless of whether there is a match in the other table. If there is no match, the columns from the non-matching table will be filled with NULL values.

## CROSS JOIN
```SQL
SELECT *
FROM orders
CROSS JOIN customers
```

A cross join returns the Cartesian product of two tables, which is a result set that includes every possible combination of rows from both tables. A cross join does not have a join condition, so it will return all rows from both tables, regardless of whether there is a match.
I hope this helps! Let me know if you have any questions.


