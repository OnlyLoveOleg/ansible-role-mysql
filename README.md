mysql
=====

Role to install and manage MySQL server.


Role Variables
--------------

defaults/main.yml

`mysql_cfg` (OPTIONAL - full/relative path to the main config file)

`mysql_conf_d` (OPTIONAL - full/relative path to glob any other configs for conf.d)

`mysql_version: 5.7` (OPTIONAL - server version)


Example (Recommended to define in group_vars or host_vars):

```
host_vars/db01.example.org.yml
  mysql_my_cnf: host_files/db01.example.org/mysql/my.cnf
  mysql_conf_d: host_files/db01.example.org/mysql/conf.d


The actual configs:

host_files/db01.example.org/mysql
├── my.cnf
└── conf.d
    ├── replication.cnf
    └── config1.cnf
```

License
-------

MIT


Author Information
------------------

Tal Lannder

tal@pjili.org
