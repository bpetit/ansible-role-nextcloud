nextcloud
=========

Ansible role to deploy and configure a simple nextcloud instance.

Requirements
------------

You need a working mariaDB/MySQL service to talk to.

Role Variables
--------------

    nextcloud_download_url: https://download.nextcloud.com/server/releases/
    nextcloud_version: 15.0.0
    nextcloud_tarball_url: "{{ nextcloud_download_url }}/nextcloud-{{ nextcloud_version }}.zip"
    nextcloud_tarball_tmp_path: "/tmp/nextcloud-{{ nextcloud_version }}.zip"
    nextcloud_tarball_md5_sum_url: "{{ nextcloud_download_url }}/nextcloud-{{ nextcloud_version }}.zip.md5"
    nextcloud_install_path: "/var/www/nextcloud"
    nextcloud_system_user: www-data
    nextcloud_system_group: www-data
    nextcloud_server_name: nextcloud.example.org # CHANGE ME
    nextcloud_http_port: 80

Dependencies
------------

This role needs no specific ansible role to work.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: nextcloud }

License
-------

BSD

Author Information
------------------

Benoit Petit <bpetit@b0rk.in>
