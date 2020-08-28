 Ansible Role to install packages
---------------------

This is an ansible role to install some basic packages, you could need.
It should work on the most linux operating systems. Maybe it need some minor adjustments.

If this is so, please create a pull request or at least creat an issue with what is broken!

### Testing:
This role was initial written for ``Debian 9`` and ``Fedora 29``.
In Spring 2019 it was only used on ``Debian 9``, ``Ubuntu 18.04 LTS`` and ``Ubuntu 19.4``. No ``RHEL`` based Systems anymore.
In Spring 2019 it was used on ``Debian 9``, ``Ubuntu 18.04 LTS``, ``Ubuntu 19.4`` and ``centos 7``.
In 2020 it expanded to more linux Systems such as ``Debian buster`` and ``Ubuntu 20.4 LTS``.

 variables
-----------

There are some variables defined to configure the packages which should be installed.

Please have a look into ``defaults/main.yml`` for more details.

You can configure your own packages via host- or group-vars to change what packages should be installed.

have fun! And don't be evil!

### Protip:
Packages are defined as variable in the ``vars`` Folder.

 Open tasks
------------
- Some CI-Testing would be nice. Eg with docker and some common linux distributions.
