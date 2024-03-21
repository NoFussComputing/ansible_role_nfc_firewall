## 1.1.0 (2024-03-21)

### Feat

- **rules**: ability to specify conn state
- **rules**: ability to specify dest interface
- **rules**: ability to specify source interface

### Fix

- **rules**: correct templating error of missing 'space' after chain/table name
- **handler**: ensure that when new rules are created the rules file is rebuilt and iptables is restarted before reloading rules
- **rules**: added missing feat to forward to specify dest host
- **rules**: templating syntax error created invalid rules

## 1.0.1 (2024-03-16)

### Fix

- **policy**: set input and forward table default policy drop
- **rules**: ensure if rule not enabled it's config file is removed

## 1.0.0 (2024-03-16)

### BREAKING CHANGE

- Repository restructured from Ansible Role to Ansible Collection

### Feat

- **firewall**: dynamic building and loading of chain and rule files with iptables-reloader script
- Convert role to collection

### Refactor

- adjust path for iptables rules files
