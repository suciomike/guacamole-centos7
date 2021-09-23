Guacamole on CENTOS7
=========

Ansible role to install and configure Guacamole with MySQL/MariaDB.

Requirements
------------

* centos/rhel 7
* ansible >= 2.9

Role Variables
--------------

Some variables that require review:
- `guacamole_version`: Guacamole version to be installed. Currently, latest version is "1.3.0".
- `tomcat_version`: Tomcat 9 version to be installed. 
- `guacamole_mysql_root_password`: Password for root user to be created for local mariadb installation. 
- `guacamole_db_name`: Database name used by guacamole. Default is "guac_db".
- `guacamole_db_username`: Database user used by guacamole. Default is "guac_user".
- `guacamole_db_password`: Database user password used by guacamole. Default is "PASSword1234".
- `guacamole_configure_firewalld`: If set to "True", firewalld will be installed and properly configured. Default value is "True".

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: guacamole-centos7 }

Usage
-----
After installation, point your browser to: `http://IP_or_FQDN/(whatever you name guacamole)`     
Default username and password is: `guacadmin`
*(Don't forget to change it)*


License
-------

BSD

Author Information
------------------

michael@michaelurrea.com
