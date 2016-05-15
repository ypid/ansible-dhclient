Getting started
===============

.. contents::
   :local:


Example inventory
-----------------

To configure :program:`dhclient` on host given in
``debops_service_dhclient`` Ansible inventory group:

.. code:: ini

    [debops_service_dhclient]
    hostname

Example playbook
----------------

Here's an example playbook that can be used to manage :program:`dhclient`::

    ---
    - name: Configure dhclient.
      hosts: 'ypid_service_dhclient'
      become: True

      roles:

        - role: ypid.dhclient
          tags: [ 'role::dhclient' ]

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
