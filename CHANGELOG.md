## 0.1.0 (2024-02-01)

### Bug Fixes

- [d6975fec](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/d6975fec188b9f01dfc03aca08eb3ce8ff330315) - accep loopback before chains [ [!5](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/5) ]
- **kubernetes**: [8f7271ae](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/8f7271ae76dc4b1dec5c1dbc1b98dbae8780c313) - coorected vxlan port [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/4) ]
- **reloader**: [9fe0c348](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/9fe0c3488dfa86b5bf1cf77b25eef99a2de299ba) - correcte iptables-restore path [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/4) [!7](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/7) ]

### Continious Integration

- [4c25c226](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/4c25c226ca1713a75ced51de3155e874cae41134) - add documentation publish job [ [!5](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/5) ]

### Documentaton / Guides

- **readme**: [2e6f6ec4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/2e6f6ec47e2fa0d77a4cff56bb83433c1cfd66d9) - fix github badge links [ [!5](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/5) ]

### Features

- **kubernetes**: [c5d29ac6](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/c5d29ac69bad680e48fb034092b6c167e861b3dc) - add chains for calico and metallb [ [!5](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/5) [!17](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/17) [!37](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/37) ]
- **package**: [5355698b](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/5355698bc766962ded46832a8c319845f8003410) - prevent auto-update [ [!5](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/5) ]
- **chain**: [098daa5a](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/098daa5a879f72e1030e42bca1ae2a204c46053e) - configurable final rule custom jump [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/4) ]
- **chains**: [c274b23a](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/c274b23aafa80baa53194fe3cf3f7a5c7d6b0deb) - rules no longr state new only [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/4) ]
- **kubernetes**: [769c7ab4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/769c7ab4ebdcc605925dde836ac6b1eb89e96ce4) - add rule for calico bgp [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/4) ]
- **iptables**: [cd087cee](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/cd087cee4090121da2d8460e2b46da6d9e951e7b) - default policy input drop, forward drop, otput accept [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/4) [!7](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/7) ]
- **rules**: [6e6cd8c0](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/6e6cd8c0393eb3e042b7939470f69d39040c9a91) - add oracle cloud default instance rules [ [!3](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/3) ]

## 0.1.0rc0 (2023-11-06)

### Bug Fixes

- **iptables**: [dcb65618](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/dcb65618d1dad2bcff2bbd162734d2df3d66ada3) - cron is required for scheduled tasks to work, install it. [ [!2](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/2) ]
- [779f9248](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/779f9248000c6411d1e9c1362b43f88e3dc7e62f) - dont flush handlers [ [!2](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/2) ]

### Continious Integration

- [a98bd5ac](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/a98bd5acc30ffed3e98f3376d54d09745ea24379) - add initial jobs [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/1) ]

### Documentaton / Guides

- [d9973b1d](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/d9973b1d7a831d6568c7e167d943228fe58ff27e) - added docs layout [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/1) ]

### Features

- **iptables**: [bd148731](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/bd148731c48e7f1dac64624c668f84c4777254d6) - move input rel,estab to end of table. [ [!2](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/2) ]
- **netfilter_persistent**: [4e50f1d3](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/commit/4e50f1d3bd2592b0103ce37150bbe21ef3dc0ea9) - option to remove existing config. default true [ [!2](https://gitlab.com/nofusscomputing/projects/ansible/firewall/-/merge_requests/2) ]

## 0.0.1 (2023-10-28)
