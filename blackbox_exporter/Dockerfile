FROM alpine

RUN wget https://github.com/prometheus/blackbox_exporter/releases/download/v0.12.0/blackbox_exporter-0.12.0.linux-armv7.tar.gz
RUN tar zxvf blackbox_exporter-0.12.0.linux-armv7.tar.gz
RUN mkdir /root/blackbox_exporter
RUN cp blackbox_exporter-0.12.0.linux-armv7/* /root/blackbox_exporter
RUN apk update && apk add libcap
RUN setcap cap_net_raw+ep /root/blackbox_exporter/blackbox_exporter

EXPOSE 9115

CMD /root/blackbox_exporter/blackbox_exporter --config.file /root/blackbox_exporter/blackbox.yml
