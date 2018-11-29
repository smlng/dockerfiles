FROM debian:stretch
LABEL maintainer "Sebastian Meiling <s@mlng.net>"

RUN apt-get update && \
    apt-get install -y \
        git cmake g++ \
        libcmocka-dev \
        libboost-dev \
        libpcap-dev \
        libusb-1.0-0-dev

RUN mkdir -p /opt && git clone https://github.com/smlng/unstrung -b pr/deps /opt/unstrung

RUN cd /opt/unstrung && ./install-git-deps.sh

RUN cd /opt/unstrung && make && make install
 
