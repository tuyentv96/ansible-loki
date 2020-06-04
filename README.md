# Ansible Role: loki


## Description

Deploy [Loki](https://github.com/grafana/loki) log aggregation system using ansible.


## Requirements

- Ansible >= 2.7

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `loki_version` | 1.5.0 | Loki package version |
| `prometheus_skip_install` | false | Prometheus installation tasks gets skipped when set to true. |
| `loki_binary_install_dir` | "/usr/local/bin" | As parameter it takes a directory where `loki` |
| `loki_config_dir` | /etc/loki | Path to directory with loki configuration |
| `loki_db_dir` | /var/lib/loki | Path to directory with loki database |
| `loki_http_listen_address` | "0.0.0.0" | Address on which loki will be listening |
| `loki_http_listen_port` | 9100 | Http port on which loki will be listening |
| `loki_config_file` | "loki.conf.j2" | Variable used to provide custom prometheus configuration file in form of ansible template |

### Playbook
```yaml
---
- hosts: all
  roles:
  - loki
```

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.