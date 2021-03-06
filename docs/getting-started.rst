Getting started
===============

.. contents::
   :local:

.. include:: includes/all.rst


Example inventory
-----------------

To manage `kibana`, on a given host it should be included in the
``debops_service_kibana`` Ansible inventory group:

.. code:: ini

   [debops_service_kibana]
   hostname

Example playbook
----------------

Here's an example playbook that uses the ``debops-contrib.kibana`` role:

.. literalinclude:: playbooks/kibana.yml
   :language: yaml

This playbooks is shipped with this role under
:file:`docs/playbooks/kibana.yml` from which you can symlink it to your
playbook directory.
In case you use multiple `DebOps Contrib`_ roles, consider
using the `DebOps Contrib playbooks`_.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::kibana``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::kibana:repo``
  Tasks related to 3rd-party APT repository configuration.

``role::kibana:pkgs``
  Tasks related to system package management like installing or
  removing packages.
