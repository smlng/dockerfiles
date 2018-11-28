FROM alpine:latest
LABEL maintainer "Sebastian Meiling <s@mlng.net>"

RUN apk --no-cache add \
        go \
        git \
        musl-dev

RUN go get github.com/ibm-security-innovation/crosscoap/...

ENTRYPOINT [ "/root/go/bin/crosscoap" ]
