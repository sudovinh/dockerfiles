From ubuntu:latest
LABEL maintainer "Vinh Nguyen <vinh@sudovinh.com>"


RUN sudo apt-get install -y iodine

# Expose the DNS port, remember to run -p 53:53/udp
EXPOSE 53/udp

RUN sudo iodined -c -f 10.0.0.1 -P iwantfreewifi t.svbot.ws
