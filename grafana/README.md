# Grafana Dockerfile

## Description

Dockerfile to build a Grafana image for Raspberry Pi (ARMv7). Includes the
following plugin(s):

- Carpet plot

The image is built from `debian:stretch-slim` and uses the binary Grafana
release. It's trivial to update the release URL in the Dockerfile.

## Usage

Build: 

`docker build -t <image/tagname> .`

Run:

Stores the database `grafana.db` in the current directory (this is the only
file that you need to save/restore).

`docker run --restart=always -d -v $(pwd)/grafana.db:/var/lib/grafana/grafana.db --name=grafana -p 3000:3000 <image/tagname>`
