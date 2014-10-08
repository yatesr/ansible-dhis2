Role Name
========

dhis2

Role Variables
--------------
```

# Location of webapps tomcat directory, will deploy war to this dir
dhis2_tomcat_webapps: "/var/lib/{{tomcat_name}}/webapps"
# Location of dhis2 config
dhis2_dir: /opt/dhis2
# User that will run dhis2. (Default is tomcat username on system)
dhis2_user: "{{tomcat_name}}"
# Postgresql password for the dhis user
dhis2_db_password: dhis2_password

#Deploy dhis2 from local war (you probably don't want this)
dhis2_deploy: false
# location of war to deploy if above is true
dhis2_war_loc:

```

Example Playbook
-------------------------
### playbook.yml

```

---
- hosts: all
  roles:
  - ansible-dhis2

  vars:
    dhis2_dir: /home/myuser/dhis2
    dhis2_db_password: secret


```

License
-------

Apache 2.0

Author Information
------------------

Ryan Yates
