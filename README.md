# sbog/prometheus_postgres_exporter

[![Build Status](https://travis-ci.com/sorrowless/ansible_prometheus_postgres_exporter.svg?branch=master)](https://travis-ci.com/sorrowless/ansible_prometheus_postgres_exporter)
[![Ansible Role](https://img.shields.io/ansible/role/54629)](https://galaxy.ansible.com/sorrowless/prometheus_postgres_exporter)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/54629)](https://galaxy.ansible.com/sorrowless/prometheus_postgres_exporter)
[![Ansible Role](https://img.shields.io/ansible/role/d/54629)](https://galaxy.ansible.com/sorrowless/prometheus_postgres_exporter)
[![GitHub](https://img.shields.io/github/license/sorrowless/ansible_prometheus_postgres_exporter)](https://github.com/sorrowless/ansible_prometheus_postgres_exporter/blob/master/LICENSE)

An Ansible role which installs and configures [Prometheus postgres_exporter](https://github.com/prometheus-community/postgres_exporter) on Linux

## Requirements

Ansible 2.8+

## Role Variables

You can see all vars in `defaults/main.yml` vars file.

If you use docker swarm, you should specify variables for the host on which
the container is supposed to be run, and also indicate the name of the swarm
manager through which the stack will be deployed in variable
`postgres_exporter_swarm_manager`
```yaml
postgres_exporter_swarm_manager: swarm-manager01
```

## Dependencies

None

## Example Playbook

```yaml
- name: Ensure prometheus_postgres_exporter
  hosts: prometheus_postgres_exporters
  remote_user: root

  roles:
    - prometheus_postgres_exporter
```

## License

Apache 2.0

## Author Information

This role was created by [Stan Bogatkin](https://sbog.ru).
