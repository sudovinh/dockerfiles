From ubuntu:latest
LABEL maintainer "Vinh Nguyen <vinh@sudovinh.com>"


RUN apt-get update && apt-get install -y iodine net-tools iptables

RUN mkdir -p /opt/iodine
ADD start.sh /opt/iodine/start.sh

WORKDIR /opt/iodine

# Expose the DNS port, remember to run -p 53:53/udp
EXPOSE 53/udp


CMD ["./start.sh"]
