# Ansible Role: openio-etcd

Ansible role to install and configure etcd clusters.

## Example

```
- name: Install etcd cluster
  hosts: etcd_all
  become: true
  roles:
    - role: etcd
```

## Parameters

Parameter | Default | Comments
--- | --- | ---
**etcd_cluster_group** | etcd_all | the target group for etcd
**etcd_initial_cluster_token** | etcd-cluster-0 | the initial token for the cluster during bootstrap
**etcd_config_dir** | /etc/etcd | the directory for configuration files
**etcd_data_dir** | /var/lib/etcd | the directory for data files
**etcd_systemd_dir** | /etc/systemd/system/etcd.service.d | the directory for systemd files
**etcd_ip_attr** | ansible_default_ipv4.address | an attribute to get the etcd cluster members' ips (dot-separated for nested attributes, see default)
**etcd_local_address** | `ansible_default_ipv4.address` | the ip on the host
**etcd_access_method** | http | the etcd communication scheme
**etcd_peer_port** | 2380 |  the etcd port for peer communication
**etcd_client_port** | 2379 | the etcd port the clients
