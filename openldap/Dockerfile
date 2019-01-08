FROM alpine:latest
LABEL maintainer "Sebastian Meiling <s@mlng.net>"

RUN apk --no-cache add \
        openldap \
        openldap-backend-all \
        openldap-overlay-all

RUN mkdir -p /run/openldap

EXPOSE 389 636

CMD ["slapd", "-d", "5" ]
