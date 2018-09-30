# Dockerfile for snmp_exporter

## Description

Packages the ARMv7 release of snmp_exporter from the Prometheus project.

## Usage

Build:

`docker build -t <tag> .`

Run:

`docker run --restart=always -d --name snmp_exporter -v $(pwd)/snmp.yml:/root/snmp_exporter/snmp.yml -p 9116:9116 <tag>`
