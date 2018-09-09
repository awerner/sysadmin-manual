FreeBSD
#######

FreeBSD is a free and open source UNIX-like Operating System well-known for its coherent design, well-grown codebase and speed and is often used on high-load servers. Well known users are WhatsApp and Netflix.

Resources
---------

`FreeBSD on Wikipedia <https://en.wikipedia.org/wiki/FreeBSD>`_ describes the History of the operating system and gives a good overview.

https://www.freebsd.org/ is the Homepage for FreeBSD, with well-wirtten documentation for almost any aspect of the system. Its Documentation for sure is one of the strong benefits of FreeBSD

Installation of software
------------------------

``pkg`` is the binary package manager of FreeBSD:

.. code-block:: bash

   pkg install <pkgname>


If you prefer to compile the software yourself, e.g. if you need to enable build options:

.. code-block:: bash

   portsnap fetch extract # only first time running portsnap
   portsnap fetch update
   cd /usr/ports/a/b
   make config-recursive install clean


Update of software
------------------

.. code-block:: bash

   pkg update
   pkg upgrade


To update all source ports:

.. code-block:: bash

   pkg install portmaster
   portsnap fetch update
   portmaster -a


System update
-------------

.. code-block:: bash

   freebsd-update fetch
   freebsd-update install


Change system configuration
---------------------------


The main system configuration file is ``/etc/rc.conf``. FreeBSD comes with a tool that allows changing that file, showing non-default values and getting values:

.. code-block:: bash

   sysrc <key>=<value>
   sysrc -a # show only changed settings
   sysrc <key>
