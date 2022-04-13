# Graces and Johns

How the popularity of those names changed over time in the US.

The data for this notebook comes from BigQuery public data set. 

```sql
SELECT
  year,
  SUM(number) as Graces
FROM
  `bigquery-public-data.usa_names.usa_1910_current`
WHERE
  name='Grace'
GROUP BY
  year
ORDER BY year;
```

A similar SQL query got the sum of people named John grouped per year.
