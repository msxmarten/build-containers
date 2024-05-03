### BUILD CONTAINER
FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
  && apt-get install -y  \
  jq gzip unzip curl git wget software-properties-common bash \
  && rm -rf /var/lib/apt/lists/*

ENV OPENTOFU 1.7.0

RUN echo "===> Installing OpenTofu ${OPENTOFU}..." \
    && wget https://github.com/opentofu/opentofu/releases/download/v${OPENTOFU}/tofu_${OPENTOFU}_amd64.deb \
    && dpkg -i tofu_${OPENTOFU}_amd64.deb \
    && mv /usr/bin/tofu /usr/bin/terraform