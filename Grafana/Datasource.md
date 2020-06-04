# MySQL

## Datetime column as the time column
- *UTC+0 is default* in grafana
- Set time value as unix time for multi-timezone support
```mysql
# use UNIX_TIMESTAMP(columnname) in select clause

select UNIX_TIMESTAMP(created_date), val1, val2
from api_stat_log
...

```
