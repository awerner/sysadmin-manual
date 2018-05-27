# PF - FreeBSD Packet Filter

pf is a firewall originally coming from OpenBSD. Since the integration with FreeBSD, its implementation has diverged from the OpenBSD one, while most examples found on the web are very similar, the focus of this documentation lies on the FreeBSD implementation.

## Installation

pf is part of the FreeBSD base system. No Installation is required.

Enabling pf is done as such:

```bash
sysrc pf_enable=YES
sysrc pf_rules=/etc/pf.conf
sysrc pflog_enable=YES
sysrc pflog_logfile=/var/log/pflog
```



