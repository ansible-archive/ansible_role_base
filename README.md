 Ansible Role to install packages
---------------------

This is an ansible role to install some basic packages, you could need.
It should work on the most linux operating systems. Maybe it need some minor adjustments.

If this is so, please create a pull request or at least creat an issue with what is broken!

### Attention:
only testet with debian9 and fedora29.

 variables
-----------

There are some variables defined to configure the packages which should be installed.

Please have a look into ``defaults/main.yml`` for more details.

You can configure your own packages via host- or group-vars to change what packages should be installed.

have fun! And don't be evil!

