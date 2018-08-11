FROM alpine:latest

ENV GOPATH /usr/local

RUN apk --no-cache add go git musl-dev && rm -rf /var/cache/apk/*
RUN go get -u github.com/m3ng9i/ran
COPY *.pem /root/

WORKDIR /usr/local/src/github.com/pions/demo-conference/www
CMD ran -p 443\
        --cert=/root/fullchain.pem\
	--key=/root/privkey.pem
