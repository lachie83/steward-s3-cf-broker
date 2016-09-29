FROM alpine:3.4

MAINTAINER <lachlan@deis.com>

RUN apk --update add ca-certificates

ADD sample-s3-uploader /sample-s3-uploader
ADD test.jpg /test.jpg

ENTRYPOINT ["/sample-s3-uploader"]
