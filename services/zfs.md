# ZFS

{% method %}
## Installation

{% sample lang="fbsd" %}
ZFS can be selected when installing FreeBSD. No Package installation is required.
{% sample lang="deb" %}
```bash
echo "deb http://ftp.debian.org/debian stretch main contrib" > /etc/apt/sources.list
apt update
apt install zfs-dkms
```
{% endmethod %}

## Operation

### List Pools

```bash
zpool list
```

### List Datasets

```bash
zfs list
```


### Enable compression

```bash
zfs set compression=lz4 zroot
```

### Show compression ratio

```bash
zfs get compressratio
```
