FROM alpine

RUN wget https://github.com/prometheus/snmp_exporter/releases/download/v0.13.0/snmp_exporter-0.13.0.linux-armv7.tar.gz
RUN tar zxvf snmp_exporter-0.13.0.linux-armv7.tar.gz
RUN mkdir /root/snmp_exporter
RUN cp snmp_exporter-0.13.0.linux-armv7/* /root/snmp_exporter/

EXPOSE 9116

CMD /root/snmp_exporter/snmp_exporter --config.file /root/snmp_exporter/snmp.yml
