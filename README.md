Playground
=========

Role to autogenerate wrapped Playbooks and Tasks from Ansible Modules.

Dependencies
------------

None

Requirements
------------

pip:
  - jmespath

Role Variables
--------------

None

Dependencies
------------

None

Example
----------------

```YAML
- name: "Generate Playbooks and Tasks"
  hosts: all
  roles:
    - role: victorock.autogen
      autogen: "{{ lookup('ENV', 'ROLE_FULL_NAME') }}"
      autogen_repo_url: "{{ lookup('ENV', 'ROLE_REPO') }}"
      autogen_repo_branch: "{{ lookup('ENV', 'ROLE_VERSION') }}"
      autogen_plugin_namespace: "{{ lookup('ENV', 'ROLE_NAMESPACE') }}"
      autogen_path: "{{ lookup('ENV', 'ROLE_BUILD_DIR') }}"

```

License
-------

GPLv3

Author Information
------------------

Victor da Costa