FROM centos:7.9.2009
ARG GO_VERSION=1.18.10
ARG GO_PROXY=https://goproxy.com/
WORKDIR /tmp
RUN curl -L https://go.dev/dl/go${GO_VERSION}.linux-amd64.tar.gz -o go${GO_VERSION}.linux-amd64.tar.gz
RUN tar xvf /tmp/go${GO_VERSION}.linux-amd64.tar.gz
RUN mv go /usr/local/go${GO_VERSION}
RUN ln -sf /usr/local/go${GO_VERSION}/bin/go /usr/local/bin/go 
RUN ln -sf /usr/local/go${GO_VERSION}/bin/gofmt /usr/local/bin/gofmt 
RUN yum groups install -y "Development Tools"
RUN yum install -y iptables-devel
RUN mkdir -p /app
WORKDIR /app
