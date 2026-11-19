# SQL Joins | `LEFT JOIN` 

Given tables A and B, returns records from A and **all records** from B, regardless
if there is a matching record or not. 

**Unmatched** records from the right-hand side table (in this case, B) are returned 
as their default value or `NULL` (depends on column definition).

**Odering matters**. If B is *left-hand side* table, then A is the *right-hand side*
table and returns null/default missing record values.

```sql
-- Will find all customers, regardless if they have any orders.
SELECT
    c.customer_name_first,
    c.customer_name_last,
    o.order_id,
    o.order_status
FROM customer AS c
LEFT JOIN order AS o ON o.customer_id = c.customer_id

-- Alternative syntax using `LEFT OUTER JOIN` (long-form of `LEFT JOIN`).
SELECT
    c.customer_name_first,
    c.customer_name_last,
    o.order_id,
    o.order_status
FROM customer AS c
LEFT OUTER JOIN order AS o ON o.customer_id = c.customer_id
```
