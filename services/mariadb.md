# MariaDB Galera Cluster

## Tasks

### Cold restart

{% method %}

Find the node that is safe to bootraps the cluster from, look for `safe_to_bootstrap: 1`

{% sample lang="deb" %}

```bash
$ cat /var/lib/mysql/grastate.dat
# GALERA saved state
version: 2.1
uuid:    438f1f9f-6b1a-11e7-8ee6-b772e69ca864
seqno:   -1
safe_to_bootstrap: 1
```
{% endmethod %}

{% method %}

Start this node first

{% sample lang="deb" %}

```bash
$ systemctl set-environment _WSREP_NEW_CLUSTER='--wsrep-new-cluster' && systemctl start mariadb && systemctl set-environment _WSREP_NEW_CLUSTER=''
```
{% endmethod %}


Finally, start the other nodes as usual




