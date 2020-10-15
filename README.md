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
- DOCKER_LABELS:
    tag1: test
- CONTAINER_NAME: "grafana"
- DOCKER_CPU_PERIOD: 0
- DOCKER_CPU_QUOTA: 0
- DOCKER_MEMORY: 0
- CONTAINER_STATE: 'started'

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
          ADMIN_PASS: Pa$$w0rd'
        tags:
          - grafana
License
-------

BSD

Author Information
------------------

Moegui.com