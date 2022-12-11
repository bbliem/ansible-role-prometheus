# ansible-role-prometheus

Ansible role for installing Prometheus

## Variables

### Docker

- `prometheus_docker_image` [default: `prom/prometheus:v2.37.2`]
- `prometheus_blackbox_exporter_docker_image` [default: `prom/blackbox-exporter:v0.22.0`]

### General

- `prometheus_config_dir` [default: `/usr/local/etc/prometheus`]
- `prometheus_hostname` [required]
- `prometheus_web_external_url` [default: `https://{{ prometheus_hostname }}`]
- `prometheus_traefik_router_rule` [default: `Host(``{{ prometheus_hostname }}``)`]
- `prometheus_basic_auth` [required]

### Node exporter

- `prometheus_node_static_configs` [required]

### Blackbox exporter
- `prometheus_blackbox_http_get_targets` [required]
- `prometheus_blackbox_http_head_targets` [required]
- `prometheus_blackbox_mastodon_instance_info_regexp` [required]
- `prometheus_blackbox_mastodon_instance_info_targets` [required]
- `prometheus_blackbox_mastodon_well_known_host_meta_regexp` [required]
- `prometheus_blackbox_mastodon_well_known_host_meta_targets` [required]
