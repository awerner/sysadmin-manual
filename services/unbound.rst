Unbound DNS
###########

Unbound is a lightweight and secure DNS server, licensed under the BSD license.

Installation
------------

.. content-tabs::

    .. tab-container:: freebsd
        :title: FreeBSD

        Unbound is in part of the system. No installation required.

    .. tab-container:: debian
        :title: Debian

        .. code-block:: bash

           apt install unbound


Configuration
-------------

The most common configuration of unbound uses the root nameservers to find out about which nameserver is the authorative for a specific domain. Unbound comes with a list of root nameservers built-in, but this may become outdated. It is therefore good practice to fetch a current list of nameservers and keep it updated.


Root Nameserver list
++++++++++++++++++++

.. content-tabs::

    .. tab-container:: freebsd
        :title: FreeBSD

        .. code-block:: bash

           wget https://www.internic.net/domain/named.cache -O /var/unbound/etc/root.hints

    .. tab-container:: debian
        :title: Debian

        .. code-block:: bash

           wget https://www.internic.net/domain/named.cache -O /etc/unbound/root.hints
