# Lightweight deployment

## Scratch
- https://hub.docker.com/_/scratch
- 'minimal' linux : less than 1 MiB
- would be a good choice for *standalone binary* distribution

### build options for scratch
- https://lynlab.co.kr/blog/64
```
CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -a -ldflags '-s' -o main main.go
```

