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

# Hardening

- Sysctl

```bash
sysctl -w net.ipv4.conf.all.rp_filter=1
sysctl -w net.ipv4.conf.all.send_redirects=0
sysctl -w net.ipv4.conf.default.send_redirects=0
sysctl -w net.ipv4.conf.all.accept_redirects=0
sysctl -w net.ipv4.conf.all.secure_redirects=0
sysctl -w net.ipv4.conf.default.accept_redirects=0
sysctl -w net.ipv4.conf.default.secure_redirects=0
sysctl -w net.ipv4.conf.all.log_martians=1
sysctl -w net.ipv4.tcp_rfc1337=1
sysctl -w net.ipv4.ip_local_port_range="32768 65535"
sysctl -w net.ipv6.conf.all.router_solicitations=0
sysctl -w net.ipv6.conf.default.router_solicitations=0
sysctl -w net.ipv6.conf.all.accept_ra_rtr_pref=0
sysctl -w net.ipv6.conf.default.accept_ra_rtr_pref=0
sysctl -w net.ipv6.conf.all.accept_ra_pinfo=0
sysctl -w net.ipv6.conf.default.accept_ra_pinfo=0
sysctl -w net.ipv6.conf.all.accept_ra_defrtr=0
sysctl -w net.ipv6.conf.default.accept_ra_defrtr=0
sysctl -w net.ipv6.conf.all.autoconf=0
sysctl -w net.ipv6.conf.default.autoconf=0
sysctl -w net.ipv6.conf.all.accept_redirects=0
sysctl -w net.ipv6.conf.default.accept_redirects=0
sysctl -w net.ipv6.conf.all.max_addresses=1
sysctl -w net.ipv6.conf.default.max_addresses=1
sysctl -w kernel.sysrq=0
sysctl -w kernel.dmesg_restrict=1
sysctl -w kernel.unprivileged_bpf_disabled=1
sysctl -w net.core.bpf_jit_harden=2
sysctl -w kernel.kexec_load_disabled=1
sysctl -w fs.suid_dumpable=0
```

- Misc

```bash
echo "readonly TMOUT=900" > /etc/profile.d/idle-users.sh
echo "readonly HISTFILE" >> /etc/profile.d/idle-users.sh
chmod +x /etc/profile.d/idle-users.sh
echo "session required pam_lastlog.so showfailed" >> /etc/pam.d/system-auth
```

