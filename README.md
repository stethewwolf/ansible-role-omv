# ansible-role-omv
Ansible role for openmediavault installation

**NB:** this role is working only for [debian bullseye](https://www.debian.org/releases/bullseye/), currently oldstable

This role require debian is installed using the [netinst](https://get.debian.org/images/archive/11.3.0/amd64/iso-cd/) whitout any
gui or web-server, only ssh and one user with sudo.

This role require [ansible-common-role](https://github.com/stethewwolf/ansible-common-role).

## Configuration
Manage the ovm version:
```
omv_version: shaitan
```

This flag must be set has false after the first run, (it is necessary skip some task)
```
omv_first_install: true
```

Manage allowed networks:
```
omv_networks:
 - 192.168.100.0/24
```
for all those networks we applay the role "ACCEPT" to all connections in input, if not define this role will applay the ACCEPT policy.

## References
* [OpenMediaVault](https://openmediavault.org)
* [OpenMediaVault - Debina installation](https://docs.openmediavault.org/en/stable/installation/on_debian.html)
