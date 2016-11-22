Getting started
===============

.. include:: includes/all.rst

.. contents::
   :local:


Example inventory
-----------------

To configure dhclient on a given host it should be included in the
``ypid_service_dhclient`` Ansible inventory group:

.. code:: ini

   [ypid_service_dhclient]
   hostname

Example playbook
----------------

Here's an example playbook that uses the ``ypid.dhclient`` role:

.. literalinclude:: playbooks/dhclient.yml
   :language: yaml

This playbook is shipped with this role under :file:`docs/playbooks/opsi.yml`
from which you can symlink it to your playbook directory.
In case you use multiple roles maintained by ypid_, consider
using `ypid-ansible-common`_.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::dhclient``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::dhclient:pkgs``
  Tasks related to system package management like installing or
  removing packages.
