FROM frappe/erpnext:v16.16.0

USER frappe
WORKDIR /home/frappe/frappe-bench

RUN git clone https://github.com/dindamajesty13/warestock.git apps/warestock
RUN bench --site all install-app warestock || true