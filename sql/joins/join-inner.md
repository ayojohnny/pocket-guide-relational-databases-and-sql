# SQL Joins | `INNER JOIN`

Given tables A and B, returns **matching** records (i.e. data found in A and B).

**Unmatched** records are dropped from the final result set.

Ordering **does not matter** on `INNER JOIN` since only matching values from both
tables are returned.

```sql
-- Only return customers who have orders.
SELECT
    c.customer_id,
    c.customer_name_first,
    c.customer_name_last,
    o.order_id,
    o.order_status,
    o.order_price_total
FROM customer AS c
INNER JOIN order AS o ON c.customer_id = o.customer_id;
```
