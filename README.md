# rvm-alpine

Dockerfile for installing RVM on Alpine Linux.

* This is a fork from Nic Doye [nicdoye/alpine-rvm]
* To keep this image minimal I'm removing building packages. If you want to use specific ruby version you probably need to install them and then remove them to keep image minimal:
```
RUN apk update \
  && apk add alpine-sdk \
  && rvm install ree \ # <-- example
  && apk del alpine-sdk  \
  && rm -rf /var/cache/apk/*

```

