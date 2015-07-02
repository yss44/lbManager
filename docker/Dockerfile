FROM phusion/golang:1.4.2-wheezy
MAINTAINER Sho Yoshida

# Build lbManager
ENV GOPATH /go
RUN go get github.com/tegioz/lbManager

# Setup lbManager runit service
RUN mkdir -p /etc/service/lbManager
ADD service_lbManager.sh /etc/service/lbManager/run
RUN chmod +x /etc/service/lbManager/run

CMD /etc/service/lbManager/run
