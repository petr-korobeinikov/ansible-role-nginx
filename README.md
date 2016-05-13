[![Build Status](https://travis-ci.org/pkorobeinikov/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/pkorobeinikov/ansible-role-nginx)

ansible-role-nginx
==================

Nginx installation.

Requirements
------------

You must provide your own configuration templates.

Role Variables
--------------

* `nginx_package_version` is an exact package version, e.g. `1.9.15-1~trusty`
* `nginx_conf_templates` is an array of config templates (see Example Playbook).

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: ansible-role-nginx
           nginx_package_version: 1.9.15-1~trusty
           nginx_conf_templates:
             - { src: nginx/nginx.conf.j2, dest: /etc/nginx/nginx.conf }
             - { src: nginx/conf.d/app.conf.j2, dest: /etc/nginx/conf.d/app.conf }


License
-------

BSD, MIT
