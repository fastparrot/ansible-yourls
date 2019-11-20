yourls
=========
This role installs and configures YOURLS.


Requirements
------------
This role requires:

	geerlingguy.apache
	geerlingguy.apache-php-fpm
	geerlingguy.php

Role Variables
--------------
* yourls_version
* yourls_www_dir
* yourls_image
* yourls_index
* yourls_db_name
* yourls_db_user
* yourls_db_host
* yourls_db_prefix
* yourls_site
* yourls_hours_offset
* yourls_lang
* yourls_unique_urls
* yourls_private
* yourls_cookiekey
* yourls_user
* yourls_pass
* yourls_debug
* yourls_url_convert
* yourls_table_url
* yourls_reserved_url
* yourls_personal_settings

[The YOURLS repo on GitHub](https://github.com/YOURLS/YOURLS/blob/master/user/config-sample.php) has more info on these settings    
There are defaults set for these variables within defaults/main.yml

Example Playbook
----------------

    - hosts: my-yourls-host
      remote_user: root
      become: yes
      become_method: sudo
      connection: ssh
      gather_facts: yes

      roles:
        - geerlingguy.apache
        - geerlingguy.php
        - geerlingguy.apache-php-fpm
        - fastparrot.yourls

Author Information
------------------

Nate Bassett
