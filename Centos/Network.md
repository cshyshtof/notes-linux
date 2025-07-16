---
type: zettel
---

```meta-bind-button
label: Set next review
hidden: false
id: review
style: primary
actions:
  - type: command
    command: review-obsidian:future-review
  - type: input
    str: "next 7 days"
```

# Network

- Configure interface

```bash
nmcli connection add type ethernet con-name infra ifname ens33 ip4 x.x.x.x/24
nmcli connection modify infra ipv4.method manual
nmcli connection modify infra ipv4.dns "1.1.1.1 8.8.8.8"
nmcli connection modify infra ipv4.dns-search "lab.local"
nmcli connection modify infra ipv4.gateway x.x.x.x
nmcli connection modify infra connection.autoconnect yes
nmcli connection modify infra connection.lldp default
nmcli connection modify infra ipv6.method ignore
nmcli connection up infra

```

- Set hostname

```bash
hostnamectl set-hostname dev
```

