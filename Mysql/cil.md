Mysql-cli csv exporting cheat sheet
- https://gist.github.com/gaerae/6219678
```
mysql -p my_db -e "SELECT * FROM my_table" | sed 's/\t/","/g;s/^/"/;s/$/"/;' > my_table.csv
```
