# Dockerfile for blackbox_exporter

## Description

Packages the ARMv7 release of blackbox_exporter from the Prometheus project.

## Usage

Build:

`docker build -t <tag> .`

Run:

`docker run --restart=always -d --name blackbox_exporter -v $(pwd)/blackbox.yml:/root/blackbox_exporter/blackbox.yml -p 9115:9115 <image>`
