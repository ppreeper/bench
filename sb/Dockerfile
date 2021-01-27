FROM ubuntu:20.04

ENV LANG C.UTF-8
ENV DEBIAN_FRONTEND noninteractive

RUN set -x; \
    apt update -y && \
    apt install sysbench fio git -y

RUN git clone https://github.com/Percona-Lab/sysbench-tpcc /sysbench-tpcc
RUN mv /sysbench-tpcc/* /usr/share/sysbench/.

RUN mkdir /data
WORKDIR /data
