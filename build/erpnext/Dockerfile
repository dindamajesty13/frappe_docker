# syntax=docker/dockerfile:1.4
FROM frappe/erpnext:v16.16.0

USER root
RUN apt-get update && apt-get install -y git openssh-client

RUN mkdir -p /root/.ssh && ssh-keyscan github.com >> /root/.ssh/known_hosts

# mount ssh key dari host saat build
RUN --mount=type=ssh \
    git clone git@github.com:dindamajesty13/warestock.git /home/frappe/frappe-bench/apps/warestock

USER frappe