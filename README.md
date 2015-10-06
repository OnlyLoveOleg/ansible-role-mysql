mysql
=====

Install and manage MySQL server.

Tested on:
 - Ubuntu Server 14.04 LTS x64


Role Variables
--------------

By default you don't need to define any variables, the role will use defaults/main.yml


defaults/main.yml

`mysql.pkg` (OPTIONAL - the package to install)

```
mysql:
  pkg: mysql-server-5.6
```

`mysql_cfg_dir` (OPTIONAL)

This is the full path to the configuration files. In this path the role expects to find
the main my.cnf file and optional conf.d directory. All files `conf.d/*.cnf` will be copied
to the remotes conf.d.

If `mysql_cfg_dir` not defined the role will use the default my.cnf from the template directory.

Example (Recommended to define in group_vars or host_vars):

```
host_vars/db01.example.org.yml
  mysql_cfg_dir: /etc/ansible/host_files/db01.example.org/mysql


The actual configs:

/etc/ansible/host_files/db01.example.org/mysql/
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

tallannder@gmail.com
