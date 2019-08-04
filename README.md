Ansible Role: Dropbox
=========

[![Build Status](https://travis-ci.org/webarchitect609/ansible-role-dropbox.svg?branch=master)](https://travis-ci.org/webarchitect609/ansible-role-dropbox)

Installs Dropbox from the [official deb repository](https://help.dropbox.com/installs-integrations/desktop/linux-commands#add).

Requirements
------------

None.

Role Variables
--------------

None of the variables need to be altered for installing the latest stable version of the application. 
However, all available variables are listed below, along with default values (see `defaults/main.yml`):

    dropbox_package: dropbox
    
Package name to install
    
    dropbox_deb_source: "deb https://linux.dropbox.com/ubuntu {{ ansible_distribution_release }} main"
    
Repository url.
    
    dropbox_gpg_key_server: "pool.sks-keyservers.net"

GPG key server. The SKS key server pool is used.
[It is not recomended](https://github.com/nginxinc/docker-nginx/issues/156) to use `pgp.mit.edu` as it may be down. 

    dropbox_gpg_key_id: "1C61A2656FB57B7E4DE0F4C1FC918B335044912E"

GPG Key ID

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: webarchitect609.dropbox }

License
-------

MIT

Author Information
------------------

This role was created in 2019 by Gripinskiy Sergey.
