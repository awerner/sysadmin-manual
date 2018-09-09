ZFS
###

Installation
------------

.. content-tabs::

    .. tab-container:: freebsd
        :title: FreeBSD

        ZFS can be selected when installing FreeBSD. No Package installation is required.

    .. tab-container:: debian
        :title: Debian

        .. code-block:: bash

           echo "deb http://ftp.debian.org/debian stretch main contrib" > /etc/apt/sources.list
           apt update
           apt install zfs-dkms


Operation
---------

List Pools
++++++++++

.. code-block:: bash

   zpool list


List Datasets
+++++++++++++

.. code-block:: bash

   zfs list



Enable compression
++++++++++++++++++

.. code-block:: bash

   zfs set compression=lz4 zroot


Show compression ratio
++++++++++++++++++++++

.. code-block:: bash

   zfs get compressratio
