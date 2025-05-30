# Ansible Zabbix S.M.A.R.T. for Zabbix agent 2

This role installs smartmontools and allows Zabbix to read S.M.A.R.T values via sudo as required by the official Template https://www.zabbix.com/integrations/smart.

### Install

```shell
ansible-galaxy install sebastian13.zabbix_smart --force 
```

### Example Playbook

```yaml
---

- name: SMART by Zabbix agent 2
  hosts: physical
  become: true

  roles:
    - role: sebastian13.zabbix_smart
```
