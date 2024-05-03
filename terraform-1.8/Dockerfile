### BUILD CONTAINER
FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
  && apt-get install -y  \
  jq gzip unzip curl git wget software-properties-common \
  && rm -rf /var/lib/apt/lists/*

ENV TERRAFORM 1.8.2

RUN echo "===> Installing Terraform ${TERRAFORM}..." \
  && curl https://releases.hashicorp.com/terraform/${TERRAFORM}/terraform_${TERRAFORM}_linux_amd64.zip -o /tmp/terraform.zip \
  && unzip /tmp/terraform.zip \
  && mv terraform /usr/local/bin/terraform \
  && rm /tmp/terraform.zip