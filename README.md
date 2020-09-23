ASBRL-GRAFANA
=========

Deploy Grafana as a Docker container and configure Prometheus as default data source.

Requirements
------------

Need to be Docker engine installed.

Role Variables
--------------

- default_user: 'ubuntu'
- PLUGIN: ''
- ROOT_URL: 'http://localhost/'
- ADMIN_PASS: 'Pa$$w0rd'
- SMTP_HOST: ''
- SMTP_USER: ''
- STMP_PASS: ''
- SMTP_FROM_ADDRESS: ''
- SMTP_FROM: ''
- BUILD: '7.1.5'
- IMAGE: 'grafana/grafana'
- PROMETHEUS_URL: 'http://localhost:9090'

Dependencies
------------

None

Example Playbook
----------------

      - name: Deploy Grafana
        include_role:
          name: asbrl-grafana
        vars:
          PROMETHEUS_URL: 'http://172.17.0.1:9090'
          ADMIN_PASS: '{{ GRAFANA_ADMIN_PASS }}'
        tags:
          - grafana
License
-------

BSD

Author Information
------------------

Moegui.com