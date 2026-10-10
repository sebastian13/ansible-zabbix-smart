# Ansible Zabbix SMART

This role installs `smartmontools` and configures the system so Zabbix Agent 2 can read S.M.A.R.T. values via `sudo`, matching the requirements of the official Zabbix template for SMART monitoring.

## Installation

Install from Ansible Galaxy:

```bash
ansible-galaxy role install sebastian13.zabbix_smart -p roles
```

Or clone it locally:

```bash
git clone https://github.com/sebastian13/ansible-zabbix-smart.git roles/zabbix_smart
```

## Example Playbook

```yaml
---
- name: Install Zabbix SMART monitoring
  hosts: physical
  become: true

  roles:
    - role: sebastian13.zabbix_smart
```

## Requirements

- Zabbix Agent 2 installed on the target host
- `sudo` available and configured to permit the Zabbix user to run SMART checks
- SMART-capable drives present on the system

## References

- [Zabbix SMART integration](https://www.zabbix.com/integrations/smart)
- [smartmontools project](https://www.smartmontools.org/)

