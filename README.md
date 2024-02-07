Ansible - SSH
=========

Ansible role for SSH managment

Requirements
------------

NA

Role Variables
--------------

No variables are needed (see `default/main.yml` file), but you need add
anything and the role check is valid and if need restart the service.

    sshd:
      custom_options:
        - "Port 22"
        - "#Include/etc/ssh/sshd_config.d/*.conf"
        - ...

Dependencies
------------

- [community.general.apk](https://docs.ansible.com/ansible/latest/collections/community/general/apk_module.html)

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-ssh, tags: [ ssh ] }

License
-------

GPLv3
