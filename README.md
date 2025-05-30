# Ansible Zabbix S.M.A.R.T. for Zabbix agent 2

This role installs smartmontools and allows Zabbix to read S.M.A.R.T values via sudo as required by the official Template https://www.zabbix.com/integrations/smart.

## Example Playbook

```yaml
---

- name: SMART by Zabbix agent 2
  hosts: physical

  roles:
    - role: sebastian13.zabbix-smart
```
