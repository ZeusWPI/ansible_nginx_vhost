NGINX vhost
=========

A role to install an NGINX vhost. Meant to be used with `ZeusWPI.nginx_base`. Just point to a vhost file and it will be copied. You can even use jinja templates if you want!

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

This example will install the vhost to `/etc/nginx/sites-available/webapp.conf`.

```
    - hosts: servers
      roles:
         - role: ZeusWPI.nginx_vhost
           nginx_vhost_src: roles/webapp/templates/webapp.nginx
           nginx_vhost_name: webapp.conf
           tags: nginx
```
If you omit the `nginx_vhost_file` variable, the basename will be used. For this example, the vhost will then be copied to `/etc/nginx/sites-available/webapp.nginx`.

License
-------

GNU General Public License v3.0

Author Information
------------------

For questions, clarifications or other chitchat, contact me at [maertensrien@gmail.com](mailto:maertensrien@gmail.com).


