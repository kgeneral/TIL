# MySQL

## Datetime column as the time column
```mysql
# use UNIX_TIMESTAMP(columnname) in select clause

select UNIX_TIMESTAMP(created_date), val1, val2
from api_stat_log
...

```
