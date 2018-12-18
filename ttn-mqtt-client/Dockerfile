FROM python:3-slim

LABEL maintainer "Sebastian Meiling <s@mlng.net>"

RUN apt-get update \
 && apt-get -y --no-install-recommends install git \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN pip3 install ttn>3 pycayennelpp

RUN mkdir -p /opt && cd /opt && git clone https://github.com/smlng/lora-tools 

ENTRYPOINT [ "python3", "/opt/lora-tools/ttn-mqtt-client/client.py" ]
