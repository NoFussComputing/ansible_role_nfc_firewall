---
title: Firewall
description: No Fuss Computings Ansible role nfc_firewall
date: 2023-10-25
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/roles/nfc_firewall
---

This role enables the setup and configuration of the firewall and fail2ban using config from code.


## Fail2ban


## Firewall

This role is designed to be included many times in your playbooks/roles and will only run install tasks once, config tasks as many times as called. With the latter containing an exception, configuring of the firewall, as it's done using a handler. This allows you to include this role many times in your playbooks or subsequent roles. All rules passed to the role on every occasion will be combined with the configuration and placement of rules done at the end of your play. This included reloading them if changed.

!!! warning Warning
    When using this role, avoid flushing the handlers as this has the possibility of generating incomplete firewall rules. Allow the handlers to run at the end of the play, as is the default.


### Role flow

1. install firewall
1. install fail2ban
1. collect any found firewall rules.
1. on handler running:
    1. if file `/etc/iptables/rules.v4.original` and `/etc/iptables/rules.v6.original`, exist create with the original contents. 
        > only runs on first run
    1. create firewall rule file and call any applicable handlers.
    1. for chain rules, add cron job to flush these tables and re-apply chain rules.
        > this is done so that any host using dns name with dynamic IP will be updated.
        > chain rule files are expected to be dynamic, therefore need to be reloaded
        > from time to time.


Default firewall rules are contained in directory `/etc/iptables/` with file names `rules.v4` and `rules.v6` for IPV4 and IPv6 respectively. This role will create these files automagically. The rules contained in this file are not intended to be reloaded periodically and should only be reloaded if the firewall rules were flushed. The intention of these files is to create the default rules, create chains and set default policy for the firewall. The granting of access through the firewall should be done via the usage of the `iptables-reloader` script. Any additional firewall rules you would like applied and updated periodically must be added to directories `/etc/iptables-reloader/.rules.d/` and `/etc/ip6tables.rules.d/` for IPv4 and IPv6 rules respectively. Should these rules need to be removed first, add the applicable command in the rules file.

!!! danger Security
    If you don't configure any firewall rules or enable any of the included rules, the default rule files `rules.v4` and `rules.v6` will not be created. This is by design and was done so, to prevent a set of firewall rules from blocking access to the machine they are applied to.

    As a consequence, the configured machine will **not have any firewall rules** which will allow anyone with network access to access any port on the machine. 

Firewall reloader script is created by this role and is located at `/bin/iptables-reloader`. Calling `sudo iptables-reloader` all firewall rules located in directories `/etc/iptables-reloader/.rules.d` and `/etc/ip6tables.rules.d` will be reapplied and without flushing the existing rules. The processing of rules is alphanumerically ordered. If sub-directories exist, the files inside them will also be applied in the same order. If an error occurs during the loading of rules, services `netfilter-persistent` and `fail2ban` (if installed) are restarted as this'll recreate the default rules and tables hopefully allowing the access rules to be re-applied.


### Troubleshooting

This role included a script located at `/bin/iptables-reloader` and calling it `sudo iptables-reloader` should fix most issues, with the exception of miss-configuration.


#### netfilter-persistent fails to start


#### fail2ban chains and/or rules missing


#### Access rules are missing

