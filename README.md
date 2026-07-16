NOTES
=====

a2enconf | a2disconf
--------------------

Because RedHat Enterprise Linux variants don't natively use a conf-enabled vs conf-available layout (everything inside /etc/httpd/conf.d/ is read automatically by default), setting a configuration to state: "disabled" in the RedHat configuration will safely delete the file from conf.d, effectively disabling it.

EXAMPLES
========

Nextcloud
---------

```yml
apache_sites:
- name:
  state:
  template:
  server_admin: support@unonweb.de
  server_name: nextcloud.unonweb.de
  document_root: /var/www/nextcloud
  remote_ip_trusted_proxy: 192.168.178.12
```