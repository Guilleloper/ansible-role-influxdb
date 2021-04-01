# ANSIBLE ROLE INFLUXDB

## Description
Ansible role for InfluxDB deployment.

(See InfluxDB repository: https://github.com/influxdata/influxdb)
<br/><br/>

## Prepare an Ansible environment for deploying the role
Steps to prepare an Ansible environment for deploying the role:
```
$ cd <deployment location>
$ view influxdb.yml
~
---
- hosts: influxdb
  become: True
  gather_facts: False
  roles:
    - influxdb
...
~
$ mkdir roles
$ cd roles/
$ git clone https://github.com/Guilleloper/ansible-role-influxdb
$ mv ansible-role-influxdb/ influxdb/
$ cd ..
```
<br/><br/>
## Deploy Influxdb:
```
$ ansible-playbook influxdb.yml --diff --check
$ ansible-playbook influxdb.yml --diff
```
