# SQL Joins | `RIGHT JOIN` 

Given tables A and B, returns all records from B and **all records** from A, regardless
if there is a matching record or not.

**Unmatched** records from the left-hand side table, in this case - A, are returned 
as their default value or `NULL` (depends on column definition).

Key Points:
- ordering matters. If A is right-hand side table, then B is the left-hand side table and returns null/default missing record values.

```sql
-- Will find all customers, regardless if they have any orders.
SELECT
    c.customer_name_first,
    c.customer_name_last,
    o.order_id,
    o.order_status
FROM customer AS c
RIGHT JOIN order AS o ON o.customer_id = c.customer_id

-- Alternative syntax using `LEFT OUTER JOIN` (long-form of `LEFT JOIN`).
SELECT
    c.customer_name_first,
    c.customer_name_last,
    o.order_id,
    o.order_status
FROM customer AS c
RIGHT OUTER JOIN order AS o ON o.customer_id = c.customer_id
```
