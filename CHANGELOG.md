## 1.0.0 (2024-03-16)

### BREAKING CHANGE

- Repository restructured from Ansible Role to Ansible Collection

### Feat

- **firewall**: dynamic building and loading of chain and rule files with iptables-reloader script
- Convert role to collection

### Refactor

- adjust path for iptables rules files

## 0.1.0 (2024-02-01)

### Feat

- **kubernetes**: add chains for calico and metallb
- **package**: prevent auto-update
- **chain**: configurable final rule custom jump
- **chains**: rules no longr state new only
- **kubernetes**: add rule for calico bgp
- **iptables**: default policy input drop, forward drop, otput accept
- **rules**: add oracle cloud default instance rules
- **iptables**: move input rel,estab to end of table.
- **netfilter_persistent**: option to remove existing config. default true

### Fix

- accep loopback before chains
- **kubernetes**: coorected vxlan port
- **reloader**: correcte iptables-restore path
- **iptables**: cron is required for scheduled tasks to work, install it.
- dont flush handlers

## 0.0.1 (2023-10-28)
