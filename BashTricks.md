# Bash tricks

## get human-readable date from epoch time
```bash
# read epochtime from external source (like file, ...)
$ echo "1583929030000" | xargs -I{} echo "{}/1000" | bc | xargs -I{} echo "@{}" | xargs date -d
(current date string)
```
