NGINX vhost
=========

A role to install an NGINX vhost. Meant to be used with `ZeusWPI.nginx_base`.

Requirements
------------

A working operating system.

Role Variables
--------------

Check out `defaults/main.yml`, I try to document each variable there.

Dependencies
------------

- `ZeusWPI.nginx_base`

Example Playbook
----------------

This example will install this role:

```
    - hosts: servers
      roles:
         - role: ZeusWPI.nginx_vhost
           nginx_vhost_location: roles/webapp/templates/site
           nginx_vhost_file: webapp
           tags: nginx
```
If you omit the `nginx_vhost_file` variable, the basename will be used.

License
-------

GNU General Public License v3.0

Author Information
------------------

For questions, clarifications or other chitchat, contact me at [maertensrien@gmail.com](mailto:maertensrien@gmail.com).


