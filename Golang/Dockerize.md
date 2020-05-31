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

### x509 error(https cert error from programmic httpclient) fix
- https://gist.github.com/michaelboke/564bf96f7331f35f1716b59984befc50
```
FROM golang:alpine as builder
WORKDIR /app
RUN apk update && apk upgrade && apk add --no-cache ca-certificates
RUN update-ca-certificates

#...

FROM scratch
COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
#...
```
