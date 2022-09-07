# ansible-radosgw_usage_exporter

Role for deploy Prometheus
[radosgw_usage_exporter](https://github.com/blemmenes/radosgw_usage_exporter)

## Requirements

* Ansible 3.0.0+;

Example configuration
-------------------------

```yaml
radosgw_usage_exporter:
  # tag of container https://hub.docker.com/r/blemmenes/radosgw_usage_exporter/
  # usually 'latest'
  - version: 'latest'
    # enable exporter service or not (docker service will be enabled)
    enable: 'true'
    # restart exporter service or not (docker service will be started)
    restart: 'true'
    # The configuration of exporter
    settings:
# Server URL for the RADOSGW api (example: http://objects.dreamhost.com/)
      - host: 'http://127.0.0.1:8087/'
# The entry point for an admin request URL (default is 'admin')
        admin_entry: 'admin'
# S3 access key
        access_key: ''
# S3 secret key
        secret_key: ''
# Port to listen
        port: '9242'
# Cluster name
        cluster_name: 'ceph'
```
