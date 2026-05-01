FROM frappe/erpnext:v16.16.0

USER root

RUN apt-get update && apt-get install -y git openssh-client

# SSH setup untuk GitHub
RUN mkdir -p /root/.ssh && ssh-keyscan github.com >> /root/.ssh/known_hosts

# clone private repo via SSH (WAJIB pakai SSH, bukan https)
RUN git clone git@github.com:dindamajesty13/warestock.git /home/frappe/frappe-bench/apps/warestock

USER frappe

RUN bench --site all install-app warestock
RUN bench build --production