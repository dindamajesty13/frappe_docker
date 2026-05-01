FROM frappe/erpnext:v16.16.0

USER root

RUN apt-get update && apt-get install -y git

RUN cd /home/frappe/frappe-bench && \
    bench get-app warestock https://github.com/dindamajesty13/warestock.git

USER frappe

RUN bench --site all install-app warestock || true