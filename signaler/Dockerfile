FROM alpine:latest

RUN echo bust cache

ENV GOPATH /usr/local

RUN apk --no-cache add go git musl-dev && rm -rf /var/cache/apk/*
RUN go get github.com/codegangsta/gin github.com/pions/signaler
COPY *.pem /root/

WORKDIR /usr/local/src/github.com/pions/demo-conference/signaler
CMD gin -p 443\
        --certFile=/root/fullchain.pem\
	--keyFile=/root/privkey.pem
