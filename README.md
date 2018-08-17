Role Name
=========

ownCloud is tool to share and synchronize your files across different devices. The role installs ownCloud, has the ability to update the OS and install httpd as well.

Requirements
------------

The module assumes that if you are going to use MariaDB and that you already have set it up separately. If there is no MariaDB present then set the `owncloud_setup_db` to true and it will install MariaDB.

Role Variables
--------------
Following are the nine variables used in the role:
*   `owncloud_setup_http` `false`
*   `owncloud_setup_php` `true`
*   `owncloud_update_os` `false`
*   `owncloud_setup_db` `false`
*   `owncloud_install_base` `false`
*   `owncloud_owncloud_destination` `/var/www/html`
*   `owncloud_php_version` `remi-php56`
*   `owncloud_db_password` `default`
*   `owncloud_db_user` `owncloud`
*   `owncloud_db_name` `owncloud`

License
-------
GPLv3

Steps to run Role
-----------------

To call the role, you would want to create a file.yml similar to:
```
---
- name: Install Owncloud
  hosts: webservers
  remote_user: root

  roles:
    - chris1984.owncloud_role
```

Author Information
------------------
**Chris Roberts** [Email](mailto:chrobert@redhat.com) [Twitter](https://twitter.com/cintrix84) [LinkedIn](https://www.linkedin.com/in/croberts84/)
