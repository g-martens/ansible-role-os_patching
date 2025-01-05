Role Name
=========

This role can be used to update your linux servers. for now it's only available for RedHat (including forks) and Debian.

Requirements
------------

You must collect the ansible_fact to use this role

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

slack_token:
kernel_update: false
reboot: true

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------
    - name: Update servers
      hosts: all
      become: true

      vars:
        slack_token:
        kernel_update: false
        reboot: true

      tasks:

        - name: Start update
          ansible.builtin.include_role:
            name: ansible-role-os_patching

