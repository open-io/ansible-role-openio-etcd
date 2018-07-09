# etcd Ansible Role

Ansible role to install and configure etcd clusters.


# Example

```
- name: Install etcd cluster
  hosts: etcd_all
  user: root
  roles:
    - { role: "etcd" }
```
