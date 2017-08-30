Synopsis
--------

This repository contains a sample Ansible playbook that
demonstrates how to make a "rolling release" of a load
balanced service.

The backend servers are two ubuntu machines running a docker container
each.

For this example we used a Netscaler VPX 12.0 and a user host which had ansible
installed with the netscaler modules.

There should be SSH access from the user host to the backend server nodes,
and HTTP access to the Netscaler NSIP for the NITRO API calls to run
successfully .

Also the Netscaler VPX node must be able to communicate with the backend
servers on a specified subnet.

All the addresses are defined in the inventory.txt file. Review and
change it according to your particular setup before running the playbooks.


The tutorial is hosted at `readthedocs`_.

.. _readthedocs: http://netscaler-ansible.readthedocs.io/en/latest/usage/rolling_upgrades_vpx.html

Dependencies
------------

Docker
++++++

On the backend servers install `docker` and `docker-compose`

Ansible
+++++++

On the user host install `Ansible`_.

Module dependencies
+++++++++++++++++++

On the user host install the `netscaler ansible modules`_

.. _Ansible: http://docs.ansible.com/ansible/intro_installation.html
.. _netscaler ansible modules: https://github.com/citrix/netscaler-ansible-modules
