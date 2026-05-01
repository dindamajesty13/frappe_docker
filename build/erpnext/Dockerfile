FROM frappe/erpnext:v16.16.0

USER root

RUN apt-get update && apt-get install -y git

RUN git clone https://github.com/dindamajesty13/warestock.git \
    /home/frappe/frappe-bench/apps/warestock

USER frappe

RUN bench --site all install-app warestock || true