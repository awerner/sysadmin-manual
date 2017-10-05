# Unbound DNS

Unbound is a lightweight and secure DNS server, licensed under the BSD license.

{% method %}
## Installation

{% sample lang="fbsd" %}
Unbound is in part of the system. No installation required.

{% sample lang="deb" %}
```bash
apt install unbound
```
{% endmethod %}

## Configuration

The most common configuration of unbound uses the root nameservers to find out about which nameserver is the authorative for a specific domain. Unbound comes with a list of root nameservers built-in, but this may become outdated. It is therefore good practice to fetch a current list of nameservers and keep it updated.

{% method %}
### Root Nameserver list

{% sample lang="fbsd" %}
```bash
wget https://www.internic.net/domain/named.cache -O /var/unbound/etc/root.hints
```

{% sample lang="deb" %}
```bash
wget https://www.internic.net/domain/named.cache -O /etc/unbound/root.hints
```

{% endmethod %}

